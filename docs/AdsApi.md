# \AdsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**boost_post**](AdsApi.md#boost_post) | **POST** /v1/ads/boost | Boost post as ad
[**create_standalone_ad**](AdsApi.md#create_standalone_ad) | **POST** /v1/ads/create | Create standalone ad
[**delete_ad**](AdsApi.md#delete_ad) | **DELETE** /v1/ads/{adId} | Cancel an ad
[**get_ad**](AdsApi.md#get_ad) | **GET** /v1/ads/{adId} | Get ad details
[**get_ad_analytics**](AdsApi.md#get_ad_analytics) | **GET** /v1/ads/{adId}/analytics | Get ad analytics
[**list_ad_accounts**](AdsApi.md#list_ad_accounts) | **GET** /v1/ads/accounts | List ad accounts
[**list_ads**](AdsApi.md#list_ads) | **GET** /v1/ads | List ads
[**list_conversion_destinations**](AdsApi.md#list_conversion_destinations) | **GET** /v1/accounts/{accountId}/conversion-destinations | List destinations for the Conversions API
[**search_ad_interests**](AdsApi.md#search_ad_interests) | **GET** /v1/ads/interests | Search targeting interests
[**send_conversions**](AdsApi.md#send_conversions) | **POST** /v1/ads/conversions | Send conversion events to an ad platform
[**update_ad**](AdsApi.md#update_ad) | **PUT** /v1/ads/{adId} | Update ad



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


## create_standalone_ad

> models::CreateStandaloneAd201Response create_standalone_ad(create_standalone_ad_request)
Create standalone ad

Creates a paid ad with custom creative. The request body supports three mutually-exclusive shapes:  1. **Legacy single-creative** (all platforms). Top-level `headline` + `body` + `imageUrl` + `linkUrl` + `callToAction` create 1 campaign + 1 ad set + 1 ad. 2. **Multi-creative** (Meta only — use `creatives[]` array). Creates 1 campaign + 1 ad set + N ads sharing the same budget / targeting / schedule. This is the standard performance-marketing creative-testing flow — Meta's delivery algorithm A/B tests the creatives inside a single ad set so budget isn't fragmented across N parallel campaigns. 3. **Attach to existing ad set** (Meta only — pass `adSetId` + a single creative). Adds one new ad to an existing ad set without creating a new campaign. Budget, targeting, goal are inherited from the ad set on Meta.  `creatives[]` and `adSetId` are mutually exclusive; specifying both returns 400.  **Per-platform required fields** (the platform is inferred from `accountId`): - **Meta (facebook, instagram)**: `accountId`, `adAccountId`, `name`, `goal`, `budgetAmount`, `budgetType`, `headline`, `body`, `imageUrl`, `linkUrl`, `callToAction`. - **Google Ads (Display)**: `accountId`, `adAccountId`, `name`, `goal`, `budgetAmount`, `budgetType`, `headline`, `body`, `linkUrl`, `images.landscape` (1.91:1) + `images.square` (1:1), `businessName`. Google's Responsive Display Ads require BOTH a landscape and a square marketing image; supplying only one is rejected by Google as \"Too few.\". The legacy top-level `imageUrl` is accepted as an alias for `images.landscape` for back-compat. `longHeadline` defaults to `headline` if omitted (max 90 chars). - **Google Ads (Search)**: `accountId`, `adAccountId`, `name`, `goal`, `budgetAmount`, `budgetType`, `headline`, `body`, `linkUrl`, `businessName`. `imageUrl` is NOT required for Search. Set `campaignType: \"search\"`. - **TikTok**: `accountId`, `adAccountId`, `name`, `goal`, `budgetAmount`, `budgetType`, `body`, `linkUrl`, `imageUrl` (this field **carries the VIDEO URL** for TikTok; the TikTok ads endpoint is video-only and the field is named `imageUrl` for cross-platform consistency). - **Pinterest**: `accountId`, `adAccountId`, `name`, `goal`, `budgetAmount`, `budgetType`, `headline`, `body`, `imageUrl`, `linkUrl`. Optional `boardId` (auto-creates \"Zernio Ads\" board if omitted). - **X / Twitter**: `accountId` (the posting account, internally resolved to the linked X Ads credential), `adAccountId`, `name`, `goal`, `budgetAmount`, `budgetType`, `body` (the tweet text, max 280 chars with `linkUrl` adding ~24). `headline`, `imageUrl`, `callToAction`, and targeting fields are ignored. Requires a connected X Ads account (`/v1/connect/twitter/ads`); otherwise 422.  **Budget minimums** are enforced per platform in USD: TikTok=$20, Pinterest=$5, all others=$1. If you pass `currency` other than USD, this minimum is currently still evaluated as USD. Pass the ad account's native currency on every request so Meta-side amount conversion is correct.  **Video ads (Meta only).** Meta (facebook, instagram) supports video creatives on all three shapes (legacy, multi-creative via `creatives[].video`, attach). Set `video: { url, thumbnailUrl }` at the request root (for legacy/attach) or per-entry inside `creatives[]` (for multi-creative). `video` and `imageUrl` are mutually exclusive per creative; supply exactly one. `video.thumbnailUrl` is required because Meta requires a thumbnail on every video creative. The video is uploaded to Meta via chunked transfer and the request blocks on Meta's transcoding (`status.video_status === 'ready'`). This path can take several minutes for longer videos; this endpoint is configured with `maxDuration = 800` on Vercel (13 min) to cover it, but your HTTP client should allow for the same. If transcoding hasn't finished within 10 minutes, the request fails with a `platform_error`. Video on non-Meta platforms is NOT supported here: TikTok uses its own flow (pass the video URL via `imageUrl`); other platforms are image-only. 

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

Returns detailed performance analytics for an ad. Includes summary metrics, a daily timeline over the requested date range, and optional demographic breakdowns (Meta and TikTok only). If no date range is provided, defaults to the last 90 days. Date range is capped at 90 days max. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_id** | **String** |  | [required] |
**from_date** | Option<**String**> | Start of date range (YYYY-MM-DD). Defaults to 90 days ago. |  |
**to_date** | Option<**String**> | End of date range (YYYY-MM-DD). Defaults to today. Max 90-day range. |  |
**breakdowns** | Option<**String**> | Comma-separated breakdown dimensions. Meta: age, gender, country, publisher_platform, device_platform, region. TikTok: gender, age, country_code, platform, ac, language. |  |

### Return type

[**models::GetAdAnalytics200Response**](getAdAnalytics_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ad_accounts

> models::ListAdAccounts200Response list_ad_accounts(account_id)
List ad accounts

Returns the platform ad accounts available for the given social account (e.g. Meta ad accounts, TikTok advertiser IDs, Google Ads customer IDs).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Social account ID | [required] |

### Return type

[**models::ListAdAccounts200Response**](listAdAccounts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ads

> models::ListAds200Response list_ads(page, limit, source, status, platform, account_id, ad_account_id, profile_id, campaign_id, from_date, to_date)
List ads

Returns a paginated list of ads with metrics computed over an optional date range. Use source=all to include externally-synced ads from platform ad managers. If no date range is provided, defaults to the last 90 days. Date range is capped at 90 days max. 

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
**from_date** | Option<**String**> | Start of metrics date range (YYYY-MM-DD). Defaults to 90 days ago. |  |
**to_date** | Option<**String**> | End of metrics date range (YYYY-MM-DD). Defaults to today. Max 90-day range. |  |

### Return type

[**models::ListAds200Response**](listAds_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_conversion_destinations

> models::ListConversionDestinations200Response list_conversion_destinations(account_id)
List destinations for the Conversions API

Returns the list of pixels (Meta) or conversion actions (Google) accessible to the connected ads account. Use the returned `id` as `destinationId` when posting to `POST /v1/ads/conversions`.  For Google, each destination's `type` reflects the conversion action's category (PURCHASE, LEAD, SIGN_UP, etc.) — the event type is locked to the destination. For Meta, `type` is absent: pixels accept any event name per request. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | SocialAccount ID (metaads or googleads). | [required] |

### Return type

[**models::ListConversionDestinations200Response**](listConversionDestinations_200_response.md)

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


## send_conversions

> models::SendConversions200Response send_conversions(send_conversions_request)
Send conversion events to an ad platform

Relay one or more conversion events to the target ad platform's native Conversions API. Supported platforms: Meta (metaads) via Graph API, Google Ads (googleads) via Data Manager API `ingestEvents`.  Platform is inferred from the provided `accountId`. `destinationId` semantics differ per platform: - Meta: pixel (dataset) ID, e.g. \"123456789012345\" - Google: conversion action resource name, e.g.   \"customers/1234567890/conversionActions/987654321\"  Callers can list valid destinations via `GET /v1/accounts/{accountId}/conversion-destinations`.  All PII (email, phone, names, external IDs) is hashed with SHA-256 server-side per each platform's normalization spec (including Google's Gmail-specific dot/plus-suffix stripping). Send plaintext.  Requires the Ads add-on.  Batching: Meta caps at 1000 events per request and rejects the entire batch if any event is malformed. Google caps at 2000. Both are handled automatically by chunking.  Dedup: pass a stable `eventId` on every event. Meta uses it to dedupe against pixel events; Google maps it to transactionId. 

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


## update_ad

> models::UpdateAd200Response update_ad(ad_id, update_ad_request)
Update ad

Update one or more fields on an ad. Status changes and budget updates are propagated to the platform. Targeting updates are Meta-only.

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

