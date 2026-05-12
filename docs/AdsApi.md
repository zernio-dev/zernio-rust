# \AdsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_conversion_associations**](AdsApi.md#add_conversion_associations) | **POST** /v1/accounts/{accountId}/conversion-destinations/{destinationId}/associations | Associate campaigns with a conversion destination
[**boost_post**](AdsApi.md#boost_post) | **POST** /v1/ads/boost | Boost post as ad
[**create_conversion_destination**](AdsApi.md#create_conversion_destination) | **POST** /v1/accounts/{accountId}/conversion-destinations | Create a conversion destination (LinkedIn)
[**create_ctwa_ad**](AdsApi.md#create_ctwa_ad) | **POST** /v1/ads/ctwa | Create Click-to-WhatsApp ad
[**create_standalone_ad**](AdsApi.md#create_standalone_ad) | **POST** /v1/ads/create | Create standalone ad
[**delete_ad**](AdsApi.md#delete_ad) | **DELETE** /v1/ads/{adId} | Cancel an ad
[**delete_conversion_destination**](AdsApi.md#delete_conversion_destination) | **DELETE** /v1/accounts/{accountId}/conversion-destinations/{destinationId} | Soft-delete a conversion destination
[**get_ad**](AdsApi.md#get_ad) | **GET** /v1/ads/{adId} | Get ad details
[**get_ad_analytics**](AdsApi.md#get_ad_analytics) | **GET** /v1/ads/{adId}/analytics | Get ad analytics
[**get_ad_comments**](AdsApi.md#get_ad_comments) | **GET** /v1/ads/{adId}/comments | List comments on an ad
[**get_conversion_destination**](AdsApi.md#get_conversion_destination) | **GET** /v1/accounts/{accountId}/conversion-destinations/{destinationId} | Fetch a single conversion destination
[**get_conversion_metrics**](AdsApi.md#get_conversion_metrics) | **GET** /v1/accounts/{accountId}/conversion-destinations/{destinationId}/metrics | Fetch attribution metrics for a conversion destination
[**list_ad_accounts**](AdsApi.md#list_ad_accounts) | **GET** /v1/ads/accounts | List ad accounts
[**list_ads**](AdsApi.md#list_ads) | **GET** /v1/ads | List ads
[**list_ads_business_centers**](AdsApi.md#list_ads_business_centers) | **GET** /v1/ads/business-centers | List TikTok Business Centers
[**list_conversion_associations**](AdsApi.md#list_conversion_associations) | **GET** /v1/accounts/{accountId}/conversion-destinations/{destinationId}/associations | List campaigns associated with a conversion destination
[**list_conversion_destinations**](AdsApi.md#list_conversion_destinations) | **GET** /v1/accounts/{accountId}/conversion-destinations | List destinations for the Conversions API
[**remove_conversion_associations**](AdsApi.md#remove_conversion_associations) | **DELETE** /v1/accounts/{accountId}/conversion-destinations/{destinationId}/associations | Remove campaign↔conversion associations
[**search_ad_interests**](AdsApi.md#search_ad_interests) | **GET** /v1/ads/interests | Search targeting interests
[**search_ad_targeting_locations**](AdsApi.md#search_ad_targeting_locations) | **GET** /v1/ads/targeting/search | Search geo targeting locations (Meta)
[**send_conversions**](AdsApi.md#send_conversions) | **POST** /v1/ads/conversions | Send conversion events to an ad platform
[**send_whats_app_conversion**](AdsApi.md#send_whats_app_conversion) | **POST** /v1/whatsapp/conversions | Send WhatsApp conversion event
[**update_ad**](AdsApi.md#update_ad) | **PUT** /v1/ads/{adId} | Update ad
[**update_conversion_destination**](AdsApi.md#update_conversion_destination) | **PATCH** /v1/accounts/{accountId}/conversion-destinations/{destinationId} | Update a conversion destination



## add_conversion_associations

> models::AddConversionAssociations200Response add_conversion_associations(account_id, destination_id, add_conversion_associations_request)
Associate campaigns with a conversion destination

Associate one or more campaigns with this conversion rule. Returns a per-campaign success/failure result so callers can retry only the rows that failed (e.g. wrong campaign type for the rule's objective). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**destination_id** | **String** |  | [required] |
**add_conversion_associations_request** | [**AddConversionAssociationsRequest**](AddConversionAssociationsRequest.md) |  | [required] |

### Return type

[**models::AddConversionAssociations200Response**](addConversionAssociations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## boost_post

> models::UpdateAd200Response boost_post(boost_post_request)
Boost post as ad

Creates a paid ad campaign from an existing published post. Creates the full platform campaign hierarchy (campaign, ad set, ad).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**boost_post_request** | [**BoostPostRequest**](BoostPostRequest.md) |  | [required] |

### Return type

[**models::UpdateAd200Response**](updateAd_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_conversion_destination

> models::CreateConversionDestination201Response create_conversion_destination(account_id, create_conversion_destination_request)
Create a conversion destination (LinkedIn)

Create a new conversion rule on the platform. LinkedIn-only today; other platforms manage destinations in their own UIs and return 405.  For LinkedIn, the rule is created with `conversionMethod=CONVERSIONS_API` and (by default) auto-associated with all of the ad account's campaigns via `autoAssociationType=ALL_CAMPAIGNS`. Pass `autoAssociationType: NONE` to opt out and manage associations explicitly via the associations endpoints below.  365-day attribution windows are only valid for `SUBMIT_APPLICATION`, `PURCHASE`, `ADD_TO_CART`, `QUALIFIED_LEAD`, and `LEAD` rule types; the API rejects other combinations locally. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | SocialAccount ID (linkedinads). | [required] |
**create_conversion_destination_request** | [**CreateConversionDestinationRequest**](CreateConversionDestinationRequest.md) |  | [required] |

### Return type

[**models::CreateConversionDestination201Response**](createConversionDestination_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_ctwa_ad

> models::CreateCtwaAd201Response create_ctwa_ad(create_ctwa_ad_request)
Create Click-to-WhatsApp ad

Creates a Click-to-WhatsApp (CTWA) ad on Meta. When tapped, the ad opens a WhatsApp conversation with the business attached to the supplied Facebook Page, and the full hierarchy (campaign, ad set, creative, ad) is created and activated in one call. The CTA is locked to WHATSAPP_MESSAGE and the destination is hard-coded to api.whatsapp.com/send; Meta resolves the actual WhatsApp number from the Page-to-WA pairing configured in Page settings or Business Manager. Prerequisites enforced by Meta (surfaced as platform_error on failure), the Facebook Page must be paired with a verified WhatsApp Business number, the WhatsApp Business Account must be business-verified, and the Meta access token must carry ads_management.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_ctwa_ad_request** | [**CreateCtwaAdRequest**](CreateCtwaAdRequest.md) |  | [required] |

### Return type

[**models::CreateCtwaAd201Response**](createCtwaAd_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_standalone_ad

> models::CreateStandaloneAd201Response create_standalone_ad(create_standalone_ad_request)
Create standalone ad

Creates a paid ad with custom creative across Meta, Google Ads, Pinterest, TikTok, and X/Twitter. Supports three mutually-exclusive request shapes selected by the body, a legacy single-creative shape (all platforms, default), a Meta-only multi-creative shape via the creatives array (one ad set with N ads sharing budget and targeting), and a Meta-only attach shape via adSetId (adds one new ad to an existing ad set). Per-platform required fields, budget minimums, and video-ad rules (Meta only) are documented on each property below.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_standalone_ad_request** | [**CreateStandaloneAdRequest**](CreateStandaloneAdRequest.md) |  | [required] |

### Return type

[**models::CreateStandaloneAd201Response**](createStandaloneAd_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_ad

> models::DeleteAccountGroup200Response delete_ad(ad_id)
Cancel an ad

Cancels the ad on the platform and marks it as cancelled in the database. The ad is preserved for history.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_id** | **String** |  | [required] |

### Return type

[**models::DeleteAccountGroup200Response**](deleteAccountGroup_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_conversion_destination

> delete_conversion_destination(account_id, destination_id, ad_account_id)
Soft-delete a conversion destination

LinkedIn-only today. LinkedIn does not expose hard-delete on conversion rules — what their UI calls \"delete\" is the same `enabled: false` flip we apply here. The rule remains fetchable via GET with `status: 'inactive'`; the unified discovery endpoint hides it by default.  `adAccountId` may be passed as a query parameter (recommended) or as a JSON body field for clients that can send DELETE bodies. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**destination_id** | **String** |  | [required] |
**ad_account_id** | Option<**String**> | Required as query OR in JSON body. |  |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad

> models::GetAd200Response get_ad(ad_id)
Get ad details

Returns an ad with its creative, targeting, status, and performance metrics.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_id** | **String** |  | [required] |

### Return type

[**models::GetAd200Response**](getAd_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad_analytics

> models::GetAdAnalytics200Response get_ad_analytics(ad_id, from_date, to_date, breakdowns)
Get ad analytics

Returns detailed performance analytics for an ad. Includes summary metrics, a daily timeline over the requested date range, and optional demographic breakdowns (Meta and TikTok only). If no date range is provided, defaults to the last 90 days. Date range is capped at 730 days max. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_id** | **String** |  | [required] |
**from_date** | Option<**String**> | Start of date range (YYYY-MM-DD). Defaults to 90 days ago. |  |
**to_date** | Option<**String**> | End of date range (YYYY-MM-DD). Defaults to today. Max 730-day range. |  |
**breakdowns** | Option<**String**> | Comma-separated breakdown dimensions. Meta: age, gender, country, publisher_platform, device_platform, region. TikTok: gender, age, country_code, platform, ac, language. |  |

### Return type

[**models::GetAdAnalytics200Response**](getAdAnalytics_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad_comments

> models::GetAdComments200Response get_ad_comments(ad_id, limit, cursor)
List comments on an ad

Returns comments on an ad's underlying creative post. Useful for moderating or analyzing engagement on dark posts (ad creatives that never went live organically), which the regular GET /v1/inbox/comments/{postId} endpoint cannot serve because dark posts are not in Zernio's post database.  Resolves the ad's creative effective_object_story_id (Facebook) or effective_instagram_media_id (Instagram) via the Marketing API on each call (cached in-process by the platform client), then fetches comments from the Graph API.  For Instagram-placed ads, the Instagram account that runs the ad must be connected to Zernio — comments are read through that account's token. If none of the connected Instagram accounts on the profile can read the ad's media, the call returns ads_connection_required.  Meta-only. Other ad platforms (TikTok, LinkedIn, Pinterest, Google, X) do not expose a public per-ad comments API and return feature_not_available.  Requires the Ads add-on. Response shape matches GET /v1/inbox/comments/{postId}. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_id** | **String** | Internal Zernio ad ID (ObjectId). | [required] |
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


## get_conversion_destination

> models::CreateConversionDestination201Response get_conversion_destination(account_id, destination_id, ad_account_id)
Fetch a single conversion destination

LinkedIn-only today. Returns the full destination record for one conversion rule. The `adAccountId` query parameter is required because LinkedIn rules are scoped to a sponsored ad account. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**destination_id** | **String** |  | [required] |
**ad_account_id** | **String** | Numeric ID or full `urn:li:sponsoredAccount:{id}` URN. | [required] |

### Return type

[**models::CreateConversionDestination201Response**](createConversionDestination_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_conversion_metrics

> models::GetConversionMetrics200Response get_conversion_metrics(account_id, destination_id, ad_account_id, start_date, end_date, granularity)
Fetch attribution metrics for a conversion destination

LinkedIn-only today. Returns conversion-attribution metrics (`externalWebsiteConversions`, `externalWebsitePostClickConversions`, `externalWebsitePostViewConversions`, `conversionValueInLocalCurrency`, `qualifiedLeads`, `costInLocalCurrency`) bucketed by date.  Date-range constraints (passed through from LinkedIn): - `granularity=DAILY` is retained for ~6 months only - `granularity=ALL` with a range > 6 months auto-rounds to month boundaries - `granularity=MONTHLY`/`YEARLY` retains 24 months  Throttle: LinkedIn caps adAnalytics at 45M metric values per 5-minute window across the calling token. Single-rule queries are well within that limit; surfaces as 429 if hit. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**destination_id** | **String** |  | [required] |
**ad_account_id** | **String** |  | [required] |
**start_date** | **String** |  | [required] |
**end_date** | Option<**String**> |  |  |
**granularity** | Option<**String**> |  |  |[default to DAILY]

### Return type

[**models::GetConversionMetrics200Response**](getConversionMetrics_200_response.md)

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


## list_ads

> models::ListAds200Response list_ads(page, limit, source, status, platform, account_id, ad_account_id, profile_id, campaign_id, platform_ad_id, effective_object_story_id, effective_instagram_media_id, from_date, to_date)
List ads

Returns a paginated list of ads with metrics computed over an optional date range. Use source=all to include externally-synced ads from platform ad managers. If no date range is provided, defaults to the last 90 days. Date range is capped at 730 days max.  To find the Zernio ad behind a comment you see in Meta Business Manager, filter by platformAdId (the Meta ad ID), effectiveObjectStoryId (Facebook), or effectiveInstagramMediaId (Instagram) — those are the post/media the ad's engagement lives on, and are also returned on each ad's `creative` object. Then call GET /v1/ads/{adId}/comments with the returned ad id. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**page** | Option<**i32**> | Page number (1-based) |  |[default to 1]
**limit** | Option<**i32**> |  |  |[default to 50]
**source** | Option<**String**> | all (default) = Zernio-created + platform-discovered ads. zernio = restrict to Zernio-created only. |  |[default to all]
**status** | Option<[**AdStatus**](AdStatus.md)> |  |  |
**platform** | Option<**String**> |  |  |
**account_id** | Option<**String**> | Social account ID |  |
**ad_account_id** | Option<**String**> | Platform ad account ID (e.g. act_123 for Meta). Mirrors the same filter on /v1/ads/campaigns and /v1/ads/tree. |  |
**profile_id** | Option<**String**> | Profile ID |  |
**campaign_id** | Option<**String**> | Platform campaign ID (filter ads within a campaign) |  |
**platform_ad_id** | Option<**String**> | Meta ad ID. Returns the ad with this platform-side ad ID. |  |
**effective_object_story_id** | Option<**String**> | Facebook `{pageId}_{postId}` of the post the ad's engagement lives on (Meta `effective_object_story_id`). Use to map a Business-Manager-visible post back to the Zernio ad. |  |
**effective_instagram_media_id** | Option<**String**> | Instagram media ID of the boosted post (Meta `effective_instagram_media_id`). Use to map a Business-Manager-visible IG post back to the Zernio ad. |  |
**from_date** | Option<**String**> | Start of metrics date range (YYYY-MM-DD). Defaults to 90 days ago. |  |
**to_date** | Option<**String**> | End of metrics date range (YYYY-MM-DD). Defaults to today. Max 730-day range. |  |

### Return type

[**models::ListAds200Response**](listAds_200_response.md)

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


## list_conversion_associations

> models::ListConversionAssociations200Response list_conversion_associations(account_id, destination_id, ad_account_id)
List campaigns associated with a conversion destination

LinkedIn-only today. Returns the campaigns currently associated with this conversion rule. Note that auto-association on rule creation runs once at create time; campaigns created after the rule still need explicit association. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**destination_id** | **String** |  | [required] |
**ad_account_id** | **String** |  | [required] |

### Return type

[**models::ListConversionAssociations200Response**](listConversionAssociations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_conversion_destinations

> models::ListConversionDestinations200Response list_conversion_destinations(account_id)
List destinations for the Conversions API

Returns the list of pixels (Meta), conversion actions (Google), or conversion rules (LinkedIn) accessible to the connected ads account. Use the returned `id` as `destinationId` when posting to `POST /v1/ads/conversions`.  For Google and LinkedIn, each destination's `type` reflects the conversion type (PURCHASE, LEAD, SIGN_UP, etc.) — the event type is locked to the destination. For Meta, `type` is absent: pixels accept any event name per request.  For LinkedIn, destinations are returned across every sponsored ad account the connected token can access; the `adAccountId` field on each destination identifies the parent ad account and is required for subsequent CRUD calls (update, delete, associations, metrics). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | SocialAccount ID (metaads, googleads, or linkedinads). | [required] |

### Return type

[**models::ListConversionDestinations200Response**](listConversionDestinations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_conversion_associations

> models::RemoveConversionAssociations200Response remove_conversion_associations(account_id, destination_id, ad_account_id, campaign_ids)
Remove campaign↔conversion associations

Remove one or more campaign associations from this conversion rule. Pass `adAccountId` and `campaignIds` as query parameters (`campaignIds` is comma-separated). The route also accepts a JSON body with the same fields for clients that prefer DELETE-with-body, but the documented surface is query-only because some SDK code generators (e.g. Python) collapse query + body parameters with the same name into a single kwarg. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**destination_id** | **String** |  | [required] |
**ad_account_id** | **String** |  | [required] |
**campaign_ids** | **String** | Comma-separated list of campaign IDs. | [required] |

### Return type

[**models::RemoveConversionAssociations200Response**](removeConversionAssociations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## search_ad_interests

> models::SearchAdInterests200Response search_ad_interests(q, account_id)
Search targeting interests

Search for interest-based targeting options available on the platform.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** | Search query | [required] |
**account_id** | **String** | Social account ID | [required] |

### Return type

[**models::SearchAdInterests200Response**](searchAdInterests_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## search_ad_targeting_locations

> models::SearchAdTargetingLocations200Response search_ad_targeting_locations(account_id, q, r#type, country_code, limit)
Search geo targeting locations (Meta)

Resolve a human-readable location name into Meta's opaque `key` used in `targeting.cities[]` / `targeting.regions[]` on `POST /v1/ads/create` (and the same fields under `targeting.geo_locations` on `POST /v1/ads/boost`). Wraps Meta's `/search?type=adgeolocation` endpoint.  Meta-only for now. Other platforms have their own location id systems and are not exposed here.  Per Meta's docs, `q` must contain only the locality name (e.g. `\"Amsterdam\"`, not `\"Amsterdam, NL\"`). Use `countryCode` to disambiguate when the same name exists in multiple countries. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Social account ID (must be a connected Facebook or Instagram account). | [required] |
**q** | **String** | Location name. Locality only — no region/country suffix. | [required] |
**r#type** | Option<**String**> | Type of location to search. Defaults to city. |  |[default to city]
**country_code** | Option<**String**> | ISO 3166-1 alpha-2 country code (e.g. NL) to scope the search. |  |
**limit** | Option<**i32**> | Maximum results to return. |  |[default to 25]

### Return type

[**models::SearchAdTargetingLocations200Response**](searchAdTargetingLocations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## send_conversions

> models::SendConversions200Response send_conversions(send_conversions_request)
Send conversion events to an ad platform

Relay one or more conversion events to the target ad platform's native Conversions API. Supported platforms: Meta (metaads) via Graph API, Google Ads (googleads) via Data Manager API `ingestEvents`, LinkedIn (linkedinads) via `/rest/conversionEvents`.  Platform is inferred from the provided `accountId`. `destinationId` semantics differ per platform: - Meta: pixel (dataset) ID, e.g. \"123456789012345\" - Google: conversion action resource name, e.g.   \"customers/1234567890/conversionActions/987654321\" - LinkedIn: conversion rule ID or URN, e.g. \"104012\" or   \"urn:lla:llaPartnerConversion:104012\"  Callers can list valid destinations via `GET /v1/accounts/{accountId}/conversion-destinations`.  All PII (email, phone, names, external IDs) is hashed with SHA-256 server-side per each platform's normalization spec (including Google's Gmail-specific dot/plus-suffix stripping). Send plaintext. Note: LinkedIn `externalIds` are passed through as plaintext per LinkedIn's spec — only emails and phones are hashed.  Requires the Ads add-on. For LinkedIn, the connected account must have been authorized after the Conversions API rollout (i.e. the OAuth grant must include `rw_conversions`); older accounts must reconnect.  Batching: Meta caps at 1000 events per request and rejects the entire batch if any event is malformed. Google caps at 2000. LinkedIn caps at 5000 and is also all-or-nothing per chunk. All three are handled automatically.  Dedup: pass a stable `eventId` on every event. Meta and LinkedIn use it to dedupe against browser-side pixel/Insight Tag events; Google maps it to transactionId.  Per-platform `eventName` semantics: - Meta: free-form. Standard names (Purchase, Lead, ...) match Meta's   built-in events; custom strings are accepted. - Google: ignored — the conversion action's category determines the   event type. Send the standard name closest to your action for   documentation, but the platform will not branch on it. - LinkedIn: ignored — the conversion rule's `type` (LEAD, PURCHASE,   etc.) is locked to the destination at rule-creation time. Send the   standard name for documentation; LinkedIn does not branch on it. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**send_conversions_request** | [**SendConversionsRequest**](SendConversionsRequest.md) |  | [required] |

### Return type

[**models::SendConversions200Response**](sendConversions_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## send_whats_app_conversion

> models::SendWhatsAppConversion200Response send_whats_app_conversion(send_whats_app_conversion_request)
Send WhatsApp conversion event

Forward a WhatsApp Business Messaging conversion event (`LeadSubmitted`, `Purchase`, `AddToCart`, `InitiateCheckout`, `ViewContent`) to Meta's Conversions API with `action_source = business_messaging` and `messaging_channel = whatsapp`. The endpoint looks up the originating CTWA click ID (`ctwa_clid`) captured on the first inbound message of the conversation and replays it on every event so Meta can attribute the conversion back to the Click-to-WhatsApp ad that drove the chat.  Configuration prerequisites on the WhatsApp account metadata:   - `metaCapiDatasetId`: the Meta Pixel/Dataset ID linked to the WABA.   - `connectedFacebookPageId`: the Facebook Page paired with the     WhatsApp Business number.  Identify the conversation by either `conversationId` (preferred) or `phoneE164` (digits only, no `+`). At least one is required. If the conversation has no captured `ctwa_clid`, the request returns 422 because there is nothing to attribute.  Token and dataset coupling: the WhatsApp account's accessToken must have access to the configured `metaCapiDatasetId`. By default a WABA's system-user token is scoped to the WABA's own Business Manager and cannot post to a pixel owned by a different Business; Meta returns code 100 in that case. Either share the dataset with the WhatsApp app's Business in BM, or use a dataset already in the same Business as the WABA. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**send_whats_app_conversion_request** | [**SendWhatsAppConversionRequest**](SendWhatsAppConversionRequest.md) |  | [required] |

### Return type

[**models::SendWhatsAppConversion200Response**](sendWhatsAppConversion_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_ad

> models::UpdateAd200Response update_ad(ad_id, update_ad_request)
Update ad

Patch one or more fields on an ad. Status, budget, targeting, and creative changes are propagated to the platform.  Per-platform support: - **Meta** (Facebook + Instagram): all fields supported. - **TikTok**: status, budget, targeting (via `/v2/adgroup/update/`), and creative   (via `/v2/ad/update/` patch-style — `headline` is ignored, `body` becomes `ad_text`). - **Pinterest / X / LinkedIn / Google**: status + budget only. Sending `targeting`   or `creative` returns 501 with code `unsupported_platform_operation`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_id** | **String** |  | [required] |
**update_ad_request** | [**UpdateAdRequest**](UpdateAdRequest.md) |  | [required] |

### Return type

[**models::UpdateAd200Response**](updateAd_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_conversion_destination

> models::CreateConversionDestination201Response update_conversion_destination(account_id, destination_id, update_conversion_destination_request)
Update a conversion destination

Partial-update a conversion rule. LinkedIn-only today. Whitelisted fields: `name`, `enabled`, attribution windows, `valueType`, `value`, `attributionType`. The rule's `type` and parent ad account are intentionally not exposed for update — recreate the rule if those need to change. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**destination_id** | **String** |  | [required] |
**update_conversion_destination_request** | [**UpdateConversionDestinationRequest**](UpdateConversionDestinationRequest.md) |  | [required] |

### Return type

[**models::CreateConversionDestination201Response**](createConversionDestination_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

