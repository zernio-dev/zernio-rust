# \AdAccountsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_account_callouts**](AdAccountsApi.md#add_account_callouts) | **POST** /v1/ads/accounts/callouts | Add account callouts
[**add_account_sitelinks**](AdAccountsApi.md#add_account_sitelinks) | **POST** /v1/ads/accounts/sitelinks | Add account sitelinks
[**add_account_structured_snippets**](AdAccountsApi.md#add_account_structured_snippets) | **POST** /v1/ads/accounts/structured-snippets | Add account snippets
[**create_ad_account**](AdAccountsApi.md#create_ad_account) | **POST** /v1/ads/accounts | Create Meta ad account
[**create_ad_negative_keyword_list**](AdAccountsApi.md#create_ad_negative_keyword_list) | **POST** /v1/ads/accounts/negative-keyword-lists | Create a negative keyword list
[**create_custom_conversion**](AdAccountsApi.md#create_custom_conversion) | **POST** /v1/accounts/{accountId}/custom-conversions | Create custom conversion
[**create_high_demand_period**](AdAccountsApi.md#create_high_demand_period) | **POST** /v1/ads/high-demand-periods | Schedule a budget increase
[**create_value_rule_set**](AdAccountsApi.md#create_value_rule_set) | **POST** /v1/ads/value-rule-sets | Create a value rule set
[**delete_ad_comment**](AdAccountsApi.md#delete_ad_comment) | **DELETE** /v1/ads/{adId}/comments/{commentId} | Delete an ad comment
[**delete_ad_negative_keyword_list**](AdAccountsApi.md#delete_ad_negative_keyword_list) | **DELETE** /v1/ads/accounts/negative-keyword-lists/{listId} | Delete a negative keyword list
[**delete_value_rule_set**](AdAccountsApi.md#delete_value_rule_set) | **DELETE** /v1/ads/value-rule-sets/{valueRuleSetId} | Delete a value rule set
[**get_ad_account_finance**](AdAccountsApi.md#get_ad_account_finance) | **GET** /v1/ads/accounts/finance | Ad account finances
[**get_ad_comments**](AdAccountsApi.md#get_ad_comments) | **GET** /v1/ads/{adId}/comments | List comments on an ad
[**get_ad_negative_keyword_list**](AdAccountsApi.md#get_ad_negative_keyword_list) | **GET** /v1/ads/accounts/negative-keyword-lists/{listId} | Get a negative keyword list
[**get_ads_activity_log**](AdAccountsApi.md#get_ads_activity_log) | **GET** /v1/ads/activity | Ad account change / audit log
[**get_dsa_defaults**](AdAccountsApi.md#get_dsa_defaults) | **GET** /v1/ads/dsa-defaults | Get ad account DSA defaults
[**get_dsa_recommendations**](AdAccountsApi.md#get_dsa_recommendations) | **GET** /v1/ads/dsa-recommendations | Get DSA recommendations
[**get_ios_fourteen_campaign_limits**](AdAccountsApi.md#get_ios_fourteen_campaign_limits) | **GET** /v1/ads/ios-fourteen-campaign-limits | Get iOS 14 campaign limits
[**get_value_rule_set**](AdAccountsApi.md#get_value_rule_set) | **GET** /v1/ads/value-rule-sets/{valueRuleSetId} | Read a value rule set
[**hide_ad_comment**](AdAccountsApi.md#hide_ad_comment) | **POST** /v1/ads/{adId}/comments/{commentId}/hide | Hide or unhide an ad comment
[**list_account_callouts**](AdAccountsApi.md#list_account_callouts) | **GET** /v1/ads/accounts/callouts | List account callouts
[**list_account_sitelinks**](AdAccountsApi.md#list_account_sitelinks) | **GET** /v1/ads/accounts/sitelinks | List account sitelinks
[**list_account_structured_snippets**](AdAccountsApi.md#list_account_structured_snippets) | **GET** /v1/ads/accounts/structured-snippets | List account snippets
[**list_ad_accounts**](AdAccountsApi.md#list_ad_accounts) | **GET** /v1/ads/accounts | List ad accounts
[**list_ad_labels**](AdAccountsApi.md#list_ad_labels) | **GET** /v1/ads/labels | Ad labels
[**list_ad_negative_keyword_lists**](AdAccountsApi.md#list_ad_negative_keyword_lists) | **GET** /v1/ads/accounts/negative-keyword-lists | List negative keyword lists
[**list_ad_studies**](AdAccountsApi.md#list_ad_studies) | **GET** /v1/ads/studies | A/B tests and lift studies
[**list_ads_business_centers**](AdAccountsApi.md#list_ads_business_centers) | **GET** /v1/ads/business-centers | List TikTok Business Centers
[**list_ads_instagram_accounts**](AdAccountsApi.md#list_ads_instagram_accounts) | **GET** /v1/ads/instagram-accounts | List Instagram ad identities
[**list_advertisable_applications**](AdAccountsApi.md#list_advertisable_applications) | **GET** /v1/ads/advertisable-applications | List advertisable apps
[**list_custom_conversions**](AdAccountsApi.md#list_custom_conversions) | **GET** /v1/accounts/{accountId}/custom-conversions | List custom conversions
[**list_high_demand_periods**](AdAccountsApi.md#list_high_demand_periods) | **GET** /v1/ads/high-demand-periods | List high-demand periods
[**list_meta_businesses**](AdAccountsApi.md#list_meta_businesses) | **GET** /v1/ads/businesses | Businesses list
[**list_tik_tok_ad_pixels**](AdAccountsApi.md#list_tik_tok_ad_pixels) | **GET** /v1/ads/pixels | List TikTok ad pixels
[**list_value_rule_sets**](AdAccountsApi.md#list_value_rule_sets) | **GET** /v1/ads/value-rule-sets | List value rule sets
[**remove_account_callout**](AdAccountsApi.md#remove_account_callout) | **DELETE** /v1/ads/accounts/callouts | Remove account callout
[**remove_account_sitelink**](AdAccountsApi.md#remove_account_sitelink) | **DELETE** /v1/ads/accounts/sitelinks | Remove account sitelink
[**remove_account_structured_snippet**](AdAccountsApi.md#remove_account_structured_snippet) | **DELETE** /v1/ads/accounts/structured-snippets | Remove account snippet
[**replace_ad_negative_keyword_list_keywords**](AdAccountsApi.md#replace_ad_negative_keyword_list_keywords) | **PUT** /v1/ads/accounts/negative-keyword-lists/{listId}/keywords | Replace negative list keywords
[**reply_to_ad_comment**](AdAccountsApi.md#reply_to_ad_comment) | **POST** /v1/ads/{adId}/comments/{commentId}/reply | Reply to an ad comment
[**update_account_callouts**](AdAccountsApi.md#update_account_callouts) | **PUT** /v1/ads/accounts/callouts | Update account callouts
[**update_account_sitelinks**](AdAccountsApi.md#update_account_sitelinks) | **PUT** /v1/ads/accounts/sitelinks | Update account sitelinks
[**update_account_structured_snippets**](AdAccountsApi.md#update_account_structured_snippets) | **PUT** /v1/ads/accounts/structured-snippets | Update account snippets
[**update_ad_account**](AdAccountsApi.md#update_ad_account) | **PATCH** /v1/ads/accounts | Update ad account settings
[**update_ad_negative_keyword_list**](AdAccountsApi.md#update_ad_negative_keyword_list) | **PUT** /v1/ads/accounts/negative-keyword-lists/{listId} | Rename a negative keyword list
[**update_value_rule_set**](AdAccountsApi.md#update_value_rule_set) | **PUT** /v1/ads/value-rule-sets/{valueRuleSetId} | Replace a value rule set



## add_account_callouts

> models::AddAccountCallouts201Response add_account_callouts(add_account_callouts_request)
Add account callouts

Creates assets and customer_asset links for this Google customer. Links apply at account level.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**add_account_callouts_request** | [**AddAccountCalloutsRequest**](AddAccountCalloutsRequest.md) |  | [required] |

### Return type

[**models::AddAccountCallouts201Response**](addAccountCallouts_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## add_account_sitelinks

> models::AddAccountSitelinks201Response add_account_sitelinks(add_account_sitelinks_request)
Add account sitelinks

Creates assets and customer_asset links for this Google customer. Links apply at account level.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**add_account_sitelinks_request** | [**AddAccountSitelinksRequest**](AddAccountSitelinksRequest.md) |  | [required] |

### Return type

[**models::AddAccountSitelinks201Response**](addAccountSitelinks_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## add_account_structured_snippets

> models::AddAccountStructuredSnippets201Response add_account_structured_snippets(add_account_structured_snippets_request)
Add account snippets

Creates assets and customer_asset links for this Google customer. Links apply at account level.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**add_account_structured_snippets_request** | [**AddAccountStructuredSnippetsRequest**](AddAccountStructuredSnippetsRequest.md) |  | [required] |

### Return type

[**models::AddAccountStructuredSnippets201Response**](addAccountStructuredSnippets_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_ad_account

> models::CreateAdAccount201Response create_ad_account(create_ad_account_request)
Create Meta ad account

Creates a durable Meta ad account in the end user's own business portfolio using their connected Meta Ads token. Requires an active metaads accountId, Ads access, business_management permission and business admin access. Discover portfolios with GET /v1/ads/businesses. System-user tokens may return an empty businesses list; supply the known business ID in that case.  The self-serve account starts without a payment method. The user must add a payment method in Ads Manager before ads can deliver. Zernio cannot add payment methods. Meta may require business verification and limits how many accounts a business can create. Closing an account does not guarantee more capacity. An ad account cannot truly be deleted, even after closing it and removing it from a business.  timezoneId is Meta's numeric ID, not an IANA timezone name. Select it from https://developers.facebook.com/docs/marketing-api/reference/ad-account/timezone-ids/. For example, 1 is America/Los_Angeles. Meta validates supported currencies and IDs. endAdvertiser, mediaAgency and partner default to NONE for the self-serve flow.  The new account is added atomically to an existing scoped ad-account allowlist. Unrestricted connections stay unrestricted. Reconnecting the same Meta identity preserves this scope unless a caller explicitly replaces it. Discovery is nudged immediately. Use the returned adAccountId with the existing ads endpoints.  This operation is not idempotent and Zernio never automatically retries it. Unknown body fields are rejected. No validateOnly or dry-run option is supported. After a timeout or a 502 with details.creationStatus=unknown, check the business in Ads Manager before attempting another creation. A 201 with connectionUpdated=false means the account exists but needs reconnecting with adAccountIds containing the returned ID and the previous scoped IDs via GET /v1/connect/facebook/ads. Do not repeat the create call. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_ad_account_request** | [**CreateAdAccountRequest**](CreateAdAccountRequest.md) |  | [required] |

### Return type

[**models::CreateAdAccount201Response**](createAdAccount_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_ad_negative_keyword_list

> models::CreateAdNegativeKeywordList201Response create_ad_negative_keyword_list(create_ad_negative_keyword_list_request)
Create a negative keyword list

Creates one Google Ads shared negative keyword list with optional initial keywords in a single atomic mutation. Daily quota is reserved for every mutate item, so large batches may return 429 before any change. This operation is not idempotent. The list is not attached to any campaign.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_ad_negative_keyword_list_request** | [**CreateAdNegativeKeywordListRequest**](CreateAdNegativeKeywordListRequest.md) |  | [required] |

### Return type

[**models::CreateAdNegativeKeywordList201Response**](createAdNegativeKeywordList_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_custom_conversion

> models::CustomConversionResult create_custom_conversion(account_id, create_custom_conversion_request)
Create custom conversion

Provision the Meta custom conversion an ads flow optimises toward, and hand back the `customConversionId` for `promotedObject.customConversionId` on POST /v1/ads/create. Removes the manual \"create it in Ads Manager first\" step.  **Reuse is ours, not Meta's.** Meta's create is not idempotent, so a retried request would otherwise mint a duplicate carrying none of the original's optimisation history. A non-archived conversion with the same `name` on the same `pixelId` is returned instead of created, with `reused: true` and a 200 rather than a 201.  `rule` is forwarded verbatim in Meta's own grammar (e.g. `{\"url\": {\"i_contains\": \"thank-you\"}}`); Meta validates it and rejects a malformed one with \"A conversion rule is required at creation time\".

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Meta ads SocialAccount id. | [required] |
**create_custom_conversion_request** | [**CreateCustomConversionRequest**](CreateCustomConversionRequest.md) |  | [required] |

### Return type

[**models::CustomConversionResult**](CustomConversionResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_high_demand_period

> models::CreateHighDemandPeriod201Response create_high_demand_period(create_high_demand_period_request)
Schedule a budget increase

Pre-schedule a temporary budget increase (Black Friday, a launch, a sale) instead of editing the budget by hand on the day. Same target rule as the GET: exactly one of `campaignId` / `adSetId`.  Two Meta constraints worth knowing before you call it. `timeStart` / `timeEnd` must fall on a 15-minute boundary, and a campaign cannot mix `ABSOLUTE` and `MULTIPLIER` across its schedules; the second type is rejected with \"Can't mix your budget scaling selection\". Window rules (must sit inside the campaign's run dates, minimum lead time, no overlap) are Meta's and its message is forwarded verbatim.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_high_demand_period_request** | [**CreateHighDemandPeriodRequest**](CreateHighDemandPeriodRequest.md) |  | [required] |

### Return type

[**models::CreateHighDemandPeriod201Response**](createHighDemandPeriod_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_value_rule_set

> models::CreateValueRuleSet201Response create_value_rule_set(create_value_rule_set_request)
Create a value rule set

Creates a value rule set on the ad account (Meta's `POST /act_X/value_rule_set`). Attach the returned id to an ad set with `valueRuleSetId` on `POST /v1/ads/create` or `PUT /v1/ads/ad-sets/{adSetId}`.  **Rule order is semantic**: rules are evaluated in array order and only the first matching rule adjusts the bid for an overlapping audience.  `adjustValue` is an unsigned magnitude in percent; the direction lives in `adjustSign`. `INCREASE` accepts 1-1000, `DECREASE` accepts 1-90. There is no signed field and 0 is out of range.  `criteriaValueTypes` is positionally paired with `criteriaValues` (same length, same order). Every type is the literal `\"NONE\"` except on `LOCATION`, which uses `LOCATION_COUNTRY` / `LOCATION_REGION` / `LOCATION_CITY` / `LOCATION_COMSCORE_MARKET` and may mix them within one criterion. Location values are Targeting-Search keys: a two-letter country code for `LOCATION_COUNTRY`, a numeric key for the rest.  `LOCATION_DMA` was replaced by `LOCATION_COMSCORE_MARKET` on 2026-06-22 and rules using DMAs are no longer active, so this API rejects it.  `AUDIENCE_LABEL` values (e.g. `HIGH_VALUE`) are applied to a Custom Audience in Ads Manager. There is no API to provision them, so label strings are passed through unvalidated and a typo produces a rule that never fires.  Ads Manager turns a rule set read-only (this API stays editable) when a rule uses more than 2 criteria, a custom age range, or the placements `FB_MARKETPLACE`, `FB_SEARCH`, `FB_VIDEO` or `IG_EXPLORE`.  Limits: 6 rule sets per ad account, 10 rules per set, 4 criteria per rule. The per-account cap is enforced by Meta, not here.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_value_rule_set_request** | [**CreateValueRuleSetRequest**](CreateValueRuleSetRequest.md) |  | [required] |

### Return type

[**models::CreateValueRuleSet201Response**](createValueRuleSet_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_ad_comment

> models::ReplyToAdComment200Response delete_ad_comment(ad_id, comment_id, since, until)
Delete an ad comment

Delete your own TikTok ad comment or reply. TikTok must return can_delete=true for the comment. Other users' comments can be hidden instead.  Unknown identity and video item fields are resolved only when needed for this action, then persisted for reuse. Comment-specific fields take precedence. If TikTok no longer returns the ad needed to resolve identity, 404 ad_not_found directs you to check deletion or archival in TikTok Ads Manager. Listing can still succeed. Unsupported or unavailable identity returns 403 feature_not_available. Denied access to ad details returns 403 insufficient_permissions with reconnect guidance and the upstream platformError.  Requires Ads access. The ad is resolved within the caller's accessible profiles. Before moderation, Zernio verifies that the comment belongs to this ad using TikTok's ad-group comment listing. The default search window is the last 30 days. Use since/until for older comments, with at most 30 days between the dates. Lookups scan at most 2,000 ad-group comments; narrow the date window if exceeded. Meta returns 501 feature_not_available with guidance to use the existing inbox comment endpoints and the account/post IDs from GET /v1/ads/{adId}/comments. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_id** | **String** | Internal Zernio ad ID or indexed platform ad ID. | [required] |
**comment_id** | **String** | TikTok comment ID from the ad comment listing. | [required] |
**since** | Option<**String**> | Start date of the comment lookup window. Defaults to 30 days before until. |  |
**until** | Option<**String**> | End date of the comment lookup window. Defaults to today in UTC. |  |

### Return type

[**models::ReplyToAdComment200Response**](replyToAdComment_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_ad_negative_keyword_list

> models::DeleteAdNegativeKeywordList200Response delete_ad_negative_keyword_list(list_id, account_id, customer_id, platform)
Delete a negative keyword list

Removes the Google shared negative keyword list. Detach it from all campaigns first; an in-use list is rejected. Only NEGATIVE_KEYWORDS shared sets are supported.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**list_id** | **String** |  | [required] |
**account_id** | **String** |  | [required] |
**customer_id** | Option<**String**> |  |  |
**platform** | Option<**String**> |  |  |

### Return type

[**models::DeleteAdNegativeKeywordList200Response**](deleteAdNegativeKeywordList_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_value_rule_set

> models::DeleteValueRuleSet200Response delete_value_rule_set(value_rule_set_id, account_id)
Delete a value rule set

Deletes the rule set (Meta's `POST /{value-rule-set-id}/delete_rule_set`, a custom action edge rather than an HTTP DELETE on its side). Ad sets pointing at it are not modified here; detach them first with `valueRulesApplied: false` on `PUT /v1/ads/ad-sets/{adSetId}`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**value_rule_set_id** | **String** | Platform value rule set id. | [required] |
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. | [required] |

### Return type

[**models::DeleteValueRuleSet200Response**](deleteValueRuleSet_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


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

> models::GetAdComments200Response get_ad_comments(ad_id, placement, limit, since, until, cursor)
List comments on an ad

Returns comments on an ad's underlying creative post. Useful for moderating or analyzing engagement on dark posts (ad creatives that never went live organically), which the regular GET /v1/inbox/comments/{postId} endpoint cannot serve because dark posts are not in Zernio's post database.  An ad that runs on both Facebook feed and Instagram feed has two separate underlying posts with separate comment threads (the creative's effective_object_story_id and effective_instagram_media_id). Use the `placement` query param to pick one; with no param the Instagram side is returned when it exists, otherwise Facebook. The identifiers are read from the ad record (persisted during sync) with a Marketing-API fallback for ads that predate the field.  For Instagram-placed comments, the Instagram account that runs the ad must be connected to Zernio, because those comments are read through that account's token. If no connected Instagram account on the profile can read the ad's media, the call returns ads_connection_required (the Facebook side, if any, is still readable via ?placement=facebook).  TikTok uses the connected TikTok Ads advertiser token and supports both paid video ads and Spark Ads. `since` and `until` select a date window of at most 30 days; the default is the last 30 days. TikTok searches by ad group, so Zernio filters each page to this ad. A page can be empty while `pagination.hasMore` is true. Reuse `pagination.cursor` with the same `limit`; the cursor retains the date window. `placement` is Meta-only and returns a 400 for TikTok. Listing needs no identity or video item ID. When the ad group is stored, each page makes one comment-list call and no ad-detail lookup, including for external ads that TikTok no longer returns from ad details. `meta.tiktokItemId: null` does not prevent listing. If the ad group is missing, Zernio fetches ad details; unavailable details return 404 ad_not_found, and no ad group returns 400 ad_not_commentable.  TikTok returns replies as separate comments with `parentId`; nested reply fetching is not supported. `canReply` requires a first-level comment, comment-management permission, a video item ID and a supported TT_USER or CUSTOMIZED_USER identity. `canDelete` requires TikTok's own-comment deletion capability, a video item ID and a supported identity. Both flags are false when identity or item is unknown. Listing uses stored and comment-specific fields without fetching identity. A direct reply or delete request can lazily resolve missing fields and succeed even after a false flag. `canHide` is true because visibility changes need only advertiser and comment IDs. `canLike` is false. Use the ad comment reply, hide and delete operations below to moderate TikTok comments. Other platforms return feature_not_available.  Requires the Ads add-on. Response shape matches GET /v1/inbox/comments/{postId}.  The `{adId}` path segment accepts any identifier dialect Zernio indexes for the ad: Zernio internal `_id` (24-char hex), the numeric `platformAdId` (the value shipped in `comment.received` webhooks as `comment.ad.id`), or the creative's `effective_object_story_id` / `effective_instagram_media_id`. Caller doesn't need a translation step. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_id** | **String** | Internal Zernio ad ID or indexed platform ad/post ID. | [required] |
**placement** | Option<**String**> | Which side of the ad to return comments for. Omit to default to the Instagram side when present, else Facebook. Returns ad_not_commentable if the ad has no such placement. |  |
**limit** | Option<**i32**> |  |  |[default to 25]
**since** | Option<**String**> | TikTok-only start date. Defaults to 30 days before until. Maximum window is 30 days. |  |
**until** | Option<**String**> | TikTok-only end date. Defaults to today in UTC. |  |
**cursor** | Option<**String**> | Pagination cursor from a previous response. |  |

### Return type

[**models::GetAdComments200Response**](getAdComments_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad_negative_keyword_list

> models::GetAdNegativeKeywordList200Response get_ad_negative_keyword_list(list_id, account_id, customer_id, platform)
Get a negative keyword list

Google Ads shared negative keyword lists (shared_set type NEGATIVE_KEYWORDS). Reads are cached for 10 minutes; quota exhaustion may return the last successful result for up to 7 days with stale=true. Customer selection is limited to this connection and its account scope. Includes the keywords and their criterion ids.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**list_id** | **String** |  | [required] |
**account_id** | **String** |  | [required] |
**customer_id** | Option<**String**> |  |  |
**platform** | Option<**String**> |  |  |

### Return type

[**models::GetAdNegativeKeywordList200Response**](getAdNegativeKeywordList_200_response.md)

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
**account_id** | **String** | Account ID (metaads, or a facebook/instagram posting account) | [required] |
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
Get DSA recommendations

Returns Meta's suggested beneficiary/payor names for an ad account, derived by Meta from the account's recent activity. Useful for prefilling `dsaBeneficiary`/`dsaPayor` inputs, or the defaults sent to `PATCH /v1/ads/accounts`, in your own UI.  Meta returns a single flat list. Entries are not labeled as beneficiary or payor, and since these are legal disclosures Zernio never applies them automatically: let your user pick the right entity. The list may be empty for accounts with little activity. Meta accounts only. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Account ID (metaads, or a facebook/instagram posting account) | [required] |
**ad_account_id** | **String** | Meta ad account ID (act_...) | [required] |

### Return type

[**models::GetDsaRecommendations200Response**](getDsaRecommendations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ios_fourteen_campaign_limits

> models::GetIosFourteenCampaignLimits200Response get_ios_fourteen_campaign_limits(account_id, ad_account_id, application_id)
Get iOS 14 campaign limits

Reads Meta iOS 14 campaign limits for an application on an ad account. applicationId is sent as Meta app_id. This read does not establish that the application is configured for iOS promotion.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Zernio Meta Ads or Facebook SocialAccount ID. | [required] |
**ad_account_id** | **String** | Meta ad account ID including the act_ prefix. | [required] |
**application_id** | **String** | Meta application ID from advertisable-applications. | [required] |

### Return type

[**models::GetIosFourteenCampaignLimits200Response**](getIosFourteenCampaignLimits_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_value_rule_set

> models::GetValueRuleSet200Response get_value_rule_set(value_rule_set_id, account_id)
Read a value rule set

Reads one value rule set including every nested rule id and criterion id. This is step one of any edit: `PUT` is a full replace, so you need the ids before you can keep the objects you are not changing.  Meta's own read returns `GENDER` values lowercase (`\"male\"`) while writes require `\"MALE\"`. Values are passed through untouched, so never case-compare a stored rule against a fetched one.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**value_rule_set_id** | **String** | Platform value rule set id. | [required] |
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. | [required] |

### Return type

[**models::GetValueRuleSet200Response**](getValueRuleSet_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## hide_ad_comment

> models::HideAdComment200Response hide_ad_comment(ad_id, comment_id, hide_ad_comment_request, since, until)
Hide or unhide an ad comment

Hide or restore a TikTok ad comment. Send hidden=true to hide it or hidden=false to make it public again. Identity and video item ID are not required; no identity lookup is performed.  Requires Ads access. The ad is resolved within the caller's accessible profiles. Before moderation, Zernio verifies that the comment belongs to this ad using TikTok's ad-group comment listing. The default search window is the last 30 days. Use since/until for older comments, with at most 30 days between the dates. Lookups scan at most 2,000 ad-group comments; narrow the date window if exceeded. Meta returns 501 feature_not_available with guidance to use the existing inbox comment endpoints and the account/post IDs from GET /v1/ads/{adId}/comments. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_id** | **String** | Internal Zernio ad ID or indexed platform ad ID. | [required] |
**comment_id** | **String** | TikTok comment ID from the ad comment listing. | [required] |
**hide_ad_comment_request** | [**HideAdCommentRequest**](HideAdCommentRequest.md) |  | [required] |
**since** | Option<**String**> | Start date of the comment lookup window. Defaults to 30 days before until. |  |
**until** | Option<**String**> | End date of the comment lookup window. Defaults to today in UTC. |  |

### Return type

[**models::HideAdComment200Response**](hideAdComment_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_account_callouts

> models::ListAccountCallouts200Response list_account_callouts(account_id, customer_id)
List account callouts

Lists directly attached Google assets. Fresh reads are cached for 10 minutes; exhausted quota may return the last successful read with stale=true. Inherited assets are not included. Preserves Google RMF C.75 account-level callouts.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**customer_id** | Option<**String**> |  |  |

### Return type

[**models::ListAccountCallouts200Response**](listAccountCallouts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_account_sitelinks

> models::ListAccountSitelinks200Response list_account_sitelinks(account_id, customer_id)
List account sitelinks

Lists directly attached Google assets. Fresh reads are cached for 10 minutes; exhausted quota may return the last successful read with stale=true. Inherited assets are not included.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**customer_id** | Option<**String**> |  |  |

### Return type

[**models::ListAccountSitelinks200Response**](listAccountSitelinks_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_account_structured_snippets

> models::ListAccountStructuredSnippets200Response list_account_structured_snippets(account_id, customer_id)
List account snippets

Lists directly attached Google assets. Fresh reads are cached for 10 minutes; exhausted quota may return the last successful read with stale=true. Inherited assets are not included.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**customer_id** | Option<**String**> |  |  |

### Return type

[**models::ListAccountStructuredSnippets200Response**](listAccountStructuredSnippets_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ad_accounts

> models::ListAdAccounts200Response list_ad_accounts(account_id, ad_account_id, limit)
List ad accounts

Returns the platform ad accounts available for the given account (e.g. Meta ad accounts, TikTok advertiser IDs, Google Ads customer IDs). Meta business-login accounts use their own system-user token. Fresh Meta discovery includes businessId and businessName from the owning Business Manager when available; cached entries gain these fields after the next discovery refresh.  For TikTok agencies: enumerates every advertiser under every Business Center the token can read (paginated server-side), then chunks the lookup against TikTok's `/advertiser/info/` endpoint (which has a per-call cap of ≤100 IDs). Solo advertisers without a BC fall back to the OAuth-time `advertiser_ids` list. Cached for 1h on the SocialAccount; lazy-refreshed on first call after expiry.  For Google Ads: responds `429` when Google's API quota is temporarily exhausted (instead of an empty list). Retry after a delay. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Account ID | [required] |
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


## list_ad_negative_keyword_lists

> models::ListAdNegativeKeywordLists200Response list_ad_negative_keyword_lists(account_id, customer_id, platform)
List negative keyword lists

Google Ads shared negative keyword lists (shared_set type NEGATIVE_KEYWORDS). Reads are cached for 10 minutes; quota exhaustion may return the last successful result for up to 7 days with stale=true. Customer selection is limited to this connection and its account scope.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**customer_id** | Option<**String**> |  |  |
**platform** | Option<**String**> |  |  |

### Return type

[**models::ListAdNegativeKeywordLists200Response**](listAdNegativeKeywordLists_200_response.md)

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
**fields** | Option<**String**> | Comma-separated Graph field override. Supports nested {} projections and Graph field modifiers, so a nested edge can be paged explicitly: without a .limit() modifier the expansion runs at the Meta default page size and the tail is dropped silently. |  |
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


## list_ads_instagram_accounts

> models::ListAdsInstagramAccounts200Response list_ads_instagram_accounts(account_id, ad_account_id)
List Instagram ad identities

Discovers identities through connected_instagram_accounts, Page linkage and Page-backed identities, with a best-effort business fallback. Business permission errors do not fail discovery. The resolved object uses the same profile-scoped resolver as ad creation; null means no identity was resolved. Format-specific observed-actor fallbacks at creative creation are not predicted.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Zernio Meta Ads or Facebook SocialAccount ID. | [required] |
**ad_account_id** | **String** | Meta ad account ID including the act_ prefix. | [required] |

### Return type

[**models::ListAdsInstagramAccounts200Response**](listAdsInstagramAccounts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_advertisable_applications

> models::ListAdvertisableApplications200Response list_advertisable_applications(account_id, ad_account_id)
List advertisable apps

Lists applications available to a Meta ad account, their supported platforms and unmodified object store URLs. A listed app still needs a configured mobile platform and store URL to run install promotion.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Zernio Meta Ads or Facebook SocialAccount ID. | [required] |
**ad_account_id** | **String** | Meta ad account ID including the act_ prefix. | [required] |

### Return type

[**models::ListAdvertisableApplications200Response**](listAdvertisableApplications_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_custom_conversions

> models::ListCustomConversions200Response list_custom_conversions(account_id, ad_account_id)
List custom conversions

The ad account's Meta custom conversions, including archived ones (`isArchived`).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Meta ads SocialAccount id. | [required] |
**ad_account_id** | **String** | Meta ad account id (act_<n>). | [required] |

### Return type

[**models::ListCustomConversions200Response**](listCustomConversions_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_high_demand_periods

> models::ListHighDemandPeriods200Response list_high_demand_periods(account_id, campaign_id, ad_set_id, limit, after)
List high-demand periods

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


## list_tik_tok_ad_pixels

> models::ListTikTokAdPixels200Response list_tik_tok_ad_pixels(account_id, advertiser_id, code)
List TikTok ad pixels

Lists pixels and their supported optimization events for a connected TikTok Ads account. The advertiser defaults to the first advertiser on the connection. Reconnect if Pixel Management permission has not been granted.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount ID. | [required] |
**advertiser_id** | Option<**String**> | Advertiser belonging to this connection. |  |
**code** | Option<**String**> | Filter by a Pixel Code. |  |

### Return type

[**models::ListTikTokAdPixels200Response**](listTikTokAdPixels_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_value_rule_sets

> models::ListValueRuleSets200Response list_value_rule_sets(account_id, ad_account_id, limit, after)
List value rule sets

Lists the ad account's value rule sets (Meta's `/act_X/value_rule_set`). A value rule set adjusts the auction bid up or down for audience segments you value differently; attach one to an ad set with `valueRuleSetId` on `POST /v1/ads/create` or `PUT /v1/ads/ad-sets/{adSetId}`.  Rows are returned in the same camelCase shape the `PUT` body takes, ids included, so a set round-trips 1:1: **the update is a full replace, not a patch**, so you GET, mutate and send the whole thing back.  Limits: 6 rule sets per ad account, 10 rules per set, 4 criteria per rule.  **Rule order is semantic.** Rules are evaluated in array order and only the FIRST matching rule adjusts the bid for an overlapping audience. The order you send is the order that is stored and returned.  Eligibility: value rule sets apply only to ad sets on the `LOWEST_COST_WITHOUT_CAP` (auto-bid) or `COST_CAP` bid strategies. Meta rejects the rest server-side.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. | [required] |
**ad_account_id** | **String** | Meta ad account id (act_<n>). | [required] |
**limit** | Option<**i32**> | Rows per page |  |[default to 25]
**after** | Option<**String**> | Cursor from paging.after of the previous page. Meta does not document paging on this edge; `after` comes back null when it omits cursors. |  |

### Return type

[**models::ListValueRuleSets200Response**](listValueRuleSets_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_account_callout

> models::RemoveAccountCallout200Response remove_account_callout(remove_account_callout_request)
Remove account callout

Removes the customer_asset attachment only. The underlying shared asset and its campaign or ad-group attachments remain.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**remove_account_callout_request** | [**RemoveAccountCalloutRequest**](RemoveAccountCalloutRequest.md) |  | [required] |

### Return type

[**models::RemoveAccountCallout200Response**](removeAccountCallout_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_account_sitelink

> models::RemoveAccountCallout200Response remove_account_sitelink(remove_account_callout_request)
Remove account sitelink

Removes the customer_asset attachment only. The underlying shared asset and its campaign or ad-group attachments remain.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**remove_account_callout_request** | [**RemoveAccountCalloutRequest**](RemoveAccountCalloutRequest.md) |  | [required] |

### Return type

[**models::RemoveAccountCallout200Response**](removeAccountCallout_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_account_structured_snippet

> models::RemoveAccountCallout200Response remove_account_structured_snippet(remove_account_callout_request)
Remove account snippet

Removes the customer_asset attachment only. The underlying shared asset and its campaign or ad-group attachments remain.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**remove_account_callout_request** | [**RemoveAccountCalloutRequest**](RemoveAccountCalloutRequest.md) |  | [required] |

### Return type

[**models::RemoveAccountCallout200Response**](removeAccountCallout_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## replace_ad_negative_keyword_list_keywords

> models::ReplaceAdNegativeKeywordListKeywords200Response replace_ad_negative_keyword_list_keywords(list_id, replace_ad_negative_keyword_list_keywords_request)
Replace negative list keywords

Replaces the full desired keyword set. Existing keywords are diffed by normalized text and match type; creates and removals are applied atomically in one mutation. Unchanged criteria retain their ids. Send an empty keywords array to clear the list. Changes affect every campaign using this list. Each create or removal consumes one daily operation; the entire batch must fit the remaining quota.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**list_id** | **String** |  | [required] |
**replace_ad_negative_keyword_list_keywords_request** | [**ReplaceAdNegativeKeywordListKeywordsRequest**](ReplaceAdNegativeKeywordListKeywordsRequest.md) |  | [required] |

### Return type

[**models::ReplaceAdNegativeKeywordListKeywords200Response**](replaceAdNegativeKeywordListKeywords_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reply_to_ad_comment

> models::ReplyToAdComment200Response reply_to_ad_comment(ad_id, comment_id, reply_to_ad_comment_request, since, until)
Reply to an ad comment

Reply to a first-level TikTok ad comment. Requires a TT_USER or CUSTOMIZED_USER identity with comment-management permission. Replies to replies are rejected. The response commentId identifies the new reply. This operation is not idempotent; do not blindly retry an uncertain response.  Unknown identity and video item fields are resolved only when needed for this action, then persisted for reuse. Comment-specific fields take precedence. If TikTok no longer returns the ad needed to resolve identity, 404 ad_not_found directs you to check deletion or archival in TikTok Ads Manager. Listing can still succeed. Unsupported or unavailable identity returns 403 feature_not_available. Denied access to ad details returns 403 insufficient_permissions with reconnect guidance and the upstream platformError.  Requires Ads access. The ad is resolved within the caller's accessible profiles. Before moderation, Zernio verifies that the comment belongs to this ad using TikTok's ad-group comment listing. The default search window is the last 30 days. Use since/until for older comments, with at most 30 days between the dates. Lookups scan at most 2,000 ad-group comments; narrow the date window if exceeded. Meta returns 501 feature_not_available with guidance to use the existing inbox comment endpoints and the account/post IDs from GET /v1/ads/{adId}/comments. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_id** | **String** | Internal Zernio ad ID or indexed platform ad ID. | [required] |
**comment_id** | **String** | TikTok comment ID from the ad comment listing. | [required] |
**reply_to_ad_comment_request** | [**ReplyToAdCommentRequest**](ReplyToAdCommentRequest.md) |  | [required] |
**since** | Option<**String**> | Start date of the comment lookup window. Defaults to 30 days before until. |  |
**until** | Option<**String**> | End date of the comment lookup window. Defaults to today in UTC. |  |

### Return type

[**models::ReplyToAdComment200Response**](replyToAdComment_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_account_callouts

> models::UpdateAccountCallouts200Response update_account_callouts(update_account_callouts_request)
Update account callouts

Edits existing Google assets in place. Send updates with assetResourceName and the fields to change. An asset is shared: changes affect every attachment using it. Omitted fields stay unchanged. The operation consumes the Google operations budget and invalidates affected cached lists.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**update_account_callouts_request** | [**UpdateAccountCalloutsRequest**](UpdateAccountCalloutsRequest.md) |  | [required] |

### Return type

[**models::UpdateAccountCallouts200Response**](updateAccountCallouts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_account_sitelinks

> models::UpdateAccountCallouts200Response update_account_sitelinks(update_account_sitelinks_request)
Update account sitelinks

Edits existing Google assets in place. Send updates with assetResourceName and the fields to change. An asset is shared: changes affect every attachment using it. Omitted fields stay unchanged. The operation consumes the Google operations budget and invalidates affected cached lists.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**update_account_sitelinks_request** | [**UpdateAccountSitelinksRequest**](UpdateAccountSitelinksRequest.md) |  | [required] |

### Return type

[**models::UpdateAccountCallouts200Response**](updateAccountCallouts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_account_structured_snippets

> models::UpdateAccountCallouts200Response update_account_structured_snippets(update_account_structured_snippets_request)
Update account snippets

Edits existing Google assets in place. Send updates with assetResourceName and the fields to change. An asset is shared: changes affect every attachment using it. Omitted fields stay unchanged. The operation consumes the Google operations budget and invalidates affected cached lists.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**update_account_structured_snippets_request** | [**UpdateAccountStructuredSnippetsRequest**](UpdateAccountStructuredSnippetsRequest.md) |  | [required] |

### Return type

[**models::UpdateAccountCallouts200Response**](updateAccountCallouts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
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


## update_ad_negative_keyword_list

> models::UpdateAdNegativeKeywordList200Response update_ad_negative_keyword_list(list_id, update_ad_negative_keyword_list_request)
Rename a negative keyword list

Renames a shared negative keyword list. Keywords and campaign associations are unchanged. Use the keywords endpoint to edit the desired keyword set.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**list_id** | **String** |  | [required] |
**update_ad_negative_keyword_list_request** | [**UpdateAdNegativeKeywordListRequest**](UpdateAdNegativeKeywordListRequest.md) |  | [required] |

### Return type

[**models::UpdateAdNegativeKeywordList200Response**](updateAdNegativeKeywordList_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_value_rule_set

> models::UpdateValueRuleSet200Response update_value_rule_set(value_rule_set_id, update_value_rule_set_request)
Replace a value rule set

**THIS IS A FULL REPLACE, NOT A PATCH.** Meta's update is declarative: the body you send becomes the rule set.  - `GET /v1/ads/value-rule-sets/{valueRuleSetId}` FIRST. - Keep a rule or criterion by echoing its `id`. - Create one by including the object WITHOUT an `id`. - Delete one by OMITTING it from the array. There is no warning and no undo.  `name` and `rules` are both required for exactly this reason: a partial body would silently destroy every rule left out.  **Rule order is semantic**: the array order you send is the evaluation order, and only the first matching rule adjusts the bid for an overlapping audience.  Existing rule sets created elsewhere may contain `LOCATION_DMA` criteria. Those went inert on 2026-06-22 and are rejected here; migrate them to `LOCATION_COMSCORE_MARKET`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**value_rule_set_id** | **String** | Platform value rule set id. | [required] |
**update_value_rule_set_request** | [**UpdateValueRuleSetRequest**](UpdateValueRuleSetRequest.md) |  | [required] |

### Return type

[**models::UpdateValueRuleSet200Response**](updateValueRuleSet_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

