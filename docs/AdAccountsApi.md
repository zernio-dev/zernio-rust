# \AdAccountsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_ad_account_finance**](AdAccountsApi.md#get_ad_account_finance) | **GET** /v1/ads/accounts/finance | Ad account finances
[**get_ad_comments**](AdAccountsApi.md#get_ad_comments) | **GET** /v1/ads/{adId}/comments | List comments on an ad
[**get_ads_activity_log**](AdAccountsApi.md#get_ads_activity_log) | **GET** /v1/ads/activity | Ad account change / audit log
[**get_dsa_defaults**](AdAccountsApi.md#get_dsa_defaults) | **GET** /v1/ads/dsa-defaults | Get ad account DSA defaults
[**get_dsa_recommendations**](AdAccountsApi.md#get_dsa_recommendations) | **GET** /v1/ads/dsa-recommendations | List DSA beneficiary/payor suggestions
[**list_ad_accounts**](AdAccountsApi.md#list_ad_accounts) | **GET** /v1/ads/accounts | List ad accounts
[**list_ad_labels**](AdAccountsApi.md#list_ad_labels) | **GET** /v1/ads/labels | Ad labels
[**list_ad_studies**](AdAccountsApi.md#list_ad_studies) | **GET** /v1/ads/studies | A/B tests and lift studies
[**list_ads_business_centers**](AdAccountsApi.md#list_ads_business_centers) | **GET** /v1/ads/business-centers | List TikTok Business Centers
[**list_high_demand_periods**](AdAccountsApi.md#list_high_demand_periods) | **GET** /v1/ads/high-demand-periods | High demand periods / budget schedules
[**list_meta_businesses**](AdAccountsApi.md#list_meta_businesses) | **GET** /v1/ads/businesses | Businesses list
[**update_ad_account**](AdAccountsApi.md#update_ad_account) | **PATCH** /v1/ads/accounts | Update ad account settings



## get_ad_account_finance

> models::GetAdAccountFinance200Response get_ad_account_finance(account_id, ad_account_id)
Ad account finances

Finances of one Meta ad account: prepaid `balance`, lifetime `amountSpent`, account `spendCap` (null = no cap) and the `fundingSource`. Money values are converted from Meta's minor units to whole units of `currency`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. | [required] |
**ad_account_id** | **String** | Meta ad account id (act_<n>). | [required] |

### Return type

[**models::GetAdAccountFinance200Response**](getAdAccountFinance_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad_comments

> models::GetAdComments200Response get_ad_comments(ad_id, placement, limit, cursor)
List comments on an ad

Returns comments on an ad's underlying creative post. Useful for moderating or analyzing engagement on dark posts (ad creatives that never went live organically), which the regular GET /v1/inbox/comments/{postId} endpoint cannot serve because dark posts are not in Zernio's post database.  An ad that runs on both Facebook feed and Instagram feed has two separate underlying posts with separate comment threads (the creative's effective_object_story_id and effective_instagram_media_id). Use the `placement` query param to pick one; with no param the Instagram side is returned when it exists, otherwise Facebook. The identifiers are read from the ad record (persisted during sync) with a Marketing-API fallback for ads that predate the field.  For Instagram-placed comments, the Instagram account that runs the ad must be connected to Zernio — those comments are read through that account's token. If no connected Instagram account on the profile can read the ad's media, the call returns ads_connection_required (the Facebook side, if any, is still readable via ?placement=facebook).  Meta-only. Other ad platforms (TikTok, LinkedIn, Pinterest, Google, X) do not expose a public per-ad comments API and return feature_not_available.  Requires the Ads add-on. Response shape matches GET /v1/inbox/comments/{postId}.  The `{adId}` path segment accepts any identifier dialect Zernio indexes for the ad: Zernio internal `_id` (24-char hex), Meta's numeric `platformAdId` (the value shipped in `comment.received` webhooks as `comment.ad.id`), or the creative's `effective_object_story_id` / `effective_instagram_media_id`. Caller doesn't need a translation step. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_id** | **String** | Internal Zernio ad ID (ObjectId). | [required] |
**placement** | Option<**String**> | Which side of the ad to return comments for. Omit to default to the Instagram side when present, else Facebook. Returns ad_not_commentable if the ad has no such placement. |  |
**limit** | Option<**i32**> |  |  |[default to 25]
**cursor** | Option<**String**> | Pagination cursor from a previous response. |  |

### Return type

[**models::GetAdComments200Response**](getAdComments_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ads_activity_log

> models::GetAdsActivityLog200Response get_ads_activity_log(account_id, ad_account_id, since, until, object_id, limit, after)
Ad account change / audit log

Account-level audit log from Meta's `/act_X/activities`: who changed what and when (creates, edits, status flips, budget changes...) with Meta's translated event names and the structured before/after in `extra_data`. Rows are returned verbatim. Meta has no server-side per-object filter on this edge, so `objectId` filters the returned page client-side (combine with paging to walk history for one campaign/ad set/ad).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. | [required] |
**ad_account_id** | **String** | Meta ad account id (act_<n>). | [required] |
**since** | Option<**String**> | Start of range (YYYY-MM-DD). |  |
**until** | Option<**String**> | End of range (YYYY-MM-DD). |  |
**object_id** | Option<**String**> | Client-side filter to one Meta object id (campaign, ad set or ad). |  |
**limit** | Option<**i32**> | Rows per page |  |[default to 50]
**after** | Option<**String**> | Cursor from paging.after of the previous page. |  |

### Return type

[**models::GetAdsActivityLog200Response**](getAdsActivityLog_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_dsa_defaults

> models::UpdateAdAccount200Response get_dsa_defaults(account_id, ad_account_id)
Get ad account DSA defaults

Returns the default DSA beneficiary and payor currently set on a Meta ad account, whether they were set via `PATCH /v1/ads/accounts` or in Meta Ads Manager. Fields are omitted when no default is configured. Meta accounts only. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Social account ID (metaads, or a facebook/instagram posting account) | [required] |
**ad_account_id** | **String** | Meta ad account ID (act_...) | [required] |

### Return type

[**models::UpdateAdAccount200Response**](updateAdAccount_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_dsa_recommendations

> models::GetDsaRecommendations200Response get_dsa_recommendations(account_id, ad_account_id)
List DSA beneficiary/payor suggestions

Returns Meta's suggested beneficiary/payor names for an ad account, derived by Meta from the account's recent activity. Useful for prefilling `dsaBeneficiary`/`dsaPayor` inputs, or the defaults sent to `PATCH /v1/ads/accounts`, in your own UI.  Meta returns a single flat list. Entries are not labeled as beneficiary or payor, and since these are legal disclosures Zernio never applies them automatically: let your user pick the right entity. The list may be empty for accounts with little activity. Meta accounts only. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Social account ID (metaads, or a facebook/instagram posting account) | [required] |
**ad_account_id** | **String** | Meta ad account ID (act_...) | [required] |

### Return type

[**models::GetDsaRecommendations200Response**](getDsaRecommendations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ad_accounts

> models::ListAdAccounts200Response list_ad_accounts(account_id, ad_account_id, limit)
List ad accounts

Returns the platform ad accounts available for the given social account (e.g. Meta ad accounts, TikTok advertiser IDs, Google Ads customer IDs).  For TikTok agencies: enumerates every advertiser under every Business Center the token can read (paginated server-side), then chunks the lookup against TikTok's `/advertiser/info/` endpoint (which has a per-call cap of ≤100 IDs). Solo advertisers without a BC fall back to the OAuth-time `advertiser_ids` list. Cached for 1h on the SocialAccount; lazy-refreshed on first call after expiry. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Social account ID | [required] |
**ad_account_id** | Option<**String**> | Filter response to a single platform ad account ID (e.g. `act_123` for Meta, advertiser_id for TikTok). Returns at most one item. |  |
**limit** | Option<**i32**> | Clamp the returned `accounts[]` length. Useful for typeahead pickers on agency tokens with hundreds of advertisers. |  |

### Return type

[**models::ListAdAccounts200Response**](listAdAccounts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ad_labels

> models::ListAdLabels200Response list_ad_labels(account_id, ad_account_id, limit, after)
Ad labels

Lists the ad account's organizational labels (Meta's `/act_X/adlabels`), rows returned verbatim (id, name, created/updated time).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. | [required] |
**ad_account_id** | **String** | Meta ad account id (act_<n>). | [required] |
**limit** | Option<**i32**> | Rows per page |  |[default to 25]
**after** | Option<**String**> | Cursor from paging.after of the previous page. |  |

### Return type

[**models::ListAdLabels200Response**](listAdLabels_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ad_studies

> models::ListAdStudies200Response list_ad_studies(account_id, ad_account_id, fields, limit, after)
A/B tests and lift studies

Lists the ad account's A/B tests and lift studies (Meta's `/act_X/ad_studies`), rows returned verbatim. The default projection covers id, name, type, timing and cells with split percentages; `fields` is a raw-passthrough override.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. | [required] |
**ad_account_id** | **String** | Meta ad account id (act_<n>). | [required] |
**fields** | Option<**String**> | Comma-separated Graph field override (supports nested {} projections). |  |
**limit** | Option<**i32**> | Rows per page |  |[default to 25]
**after** | Option<**String**> | Cursor from paging.after of the previous page. |  |

### Return type

[**models::ListAdStudies200Response**](listAdStudies_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ads_business_centers

> models::ListAdsBusinessCenters200Response list_ads_business_centers(account_id)
List TikTok Business Centers

Returns the TikTok Business Centers (BCs) the connected `tiktokads` account can read. Each BC reports its advertiser count so callers can build agency-style pickers without re-walking `/v1/ads/accounts` per BC.  TikTok-only. Solo advertisers (non-agency tokens) return an empty array. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | ID of the `tiktokads` (or parent `tiktok` posting) SocialAccount | [required] |

### Return type

[**models::ListAdsBusinessCenters200Response**](listAdsBusinessCenters_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_high_demand_periods

> models::ListHighDemandPeriods200Response list_high_demand_periods(account_id, campaign_id, ad_set_id, limit, after)
High demand periods / budget schedules

Scheduled budget increases (Meta's budget-scheduling API). The Graph edge lives on the campaign and ad-set nodes only, so exactly one of `campaignId` / `adSetId` (platform ids) is required. Rows returned verbatim (budget_value, budget_value_type, time window, recurrence).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. | [required] |
**campaign_id** | Option<**String**> | Platform campaign id. Exactly one of campaignId / adSetId. |  |
**ad_set_id** | Option<**String**> | Platform ad set id. Exactly one of campaignId / adSetId. |  |
**limit** | Option<**i32**> | Rows per page |  |[default to 25]
**after** | Option<**String**> | Cursor from paging.after of the previous page. |  |

### Return type

[**models::ListHighDemandPeriods200Response**](listHighDemandPeriods_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_meta_businesses

> models::ListMetaBusinesses200Response list_meta_businesses(account_id, limit, after)
Businesses list

Business Manager portfolios the connected Meta user belongs to (Meta's `/me/businesses`), rows returned verbatim (id, name, verification_status, created_time). Token-scoped, so no `adAccountId` is needed. For TikTok Business Centers use `GET /v1/ads/business-centers`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. | [required] |
**limit** | Option<**i32**> | Rows per page |  |[default to 25]
**after** | Option<**String**> | Cursor from paging.after of the previous page. |  |

### Return type

[**models::ListMetaBusinesses200Response**](listMetaBusinesses_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_ad_account

> models::UpdateAdAccount200Response update_ad_account(update_ad_account_request)
Update ad account settings

Sets the default DSA beneficiary and payor on a Meta ad account (EU DSA, Article 26). Set them once and every EU-targeted call to `/v1/ads/create`, `/v1/ads/boost` and `/v1/ads/ctwa` on that ad account can omit `dsaBeneficiary`/`dsaPayor`: Meta applies the defaults automatically.  The values are written to the ad account on Meta, the same setting Ads Manager edits. Nothing is stored in Zernio, and defaults already set in Ads Manager work identically. Zernio never guesses these values for you. Beneficiary and payor are legal disclosures shown to EU users, so you must provide the entity names explicitly. Use `GET /v1/ads/dsa-recommendations` to offer suggestions in your UI.  If `defaultDsaPayor` is omitted, the beneficiary is also set as the payor, which covers the common case where the same entity benefits from and pays for the ads. Read the current values back with `GET /v1/ads/dsa-defaults`.  Currently supported for Meta accounts only; other platforms return 400. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**update_ad_account_request** | [**UpdateAdAccountRequest**](UpdateAdAccountRequest.md) |  | [required] |

### Return type

[**models::UpdateAdAccount200Response**](updateAdAccount_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

