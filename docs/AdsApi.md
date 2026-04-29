# \AdsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**boost_post**](AdsApi.md#boost_post) | **POST** /v1/ads/boost | Boost post as ad
[**create_ctwa_ad**](AdsApi.md#create_ctwa_ad) | **POST** /v1/ads/ctwa | Create Click-to-WhatsApp ad
[**create_standalone_ad**](AdsApi.md#create_standalone_ad) | **POST** /v1/ads/create | Create standalone ad
[**delete_ad**](AdsApi.md#delete_ad) | **DELETE** /v1/ads/{adId} | Cancel an ad
[**get_ad**](AdsApi.md#get_ad) | **GET** /v1/ads/{adId} | Get ad details
[**get_ad_analytics**](AdsApi.md#get_ad_analytics) | **GET** /v1/ads/{adId}/analytics | Get ad analytics
[**get_ad_comments**](AdsApi.md#get_ad_comments) | **GET** /v1/ads/{adId}/comments | List comments on an ad
[**list_ad_accounts**](AdsApi.md#list_ad_accounts) | **GET** /v1/ads/accounts | List ad accounts
[**list_ads**](AdsApi.md#list_ads) | **GET** /v1/ads | List ads
[**list_conversion_destinations**](AdsApi.md#list_conversion_destinations) | **GET** /v1/accounts/{accountId}/conversion-destinations | List destinations for the Conversions API
[**search_ad_interests**](AdsApi.md#search_ad_interests) | **GET** /v1/ads/interests | Search targeting interests
[**send_conversions**](AdsApi.md#send_conversions) | **POST** /v1/ads/conversions | Send conversion events to an ad platform
[**send_whats_app_conversion**](AdsApi.md#send_whats_app_conversion) | **POST** /v1/whatsapp/conversions | Send WhatsApp conversion event
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


## get_ad_comments

> models::GetAdComments200Response get_ad_comments(ad_id, limit, cursor)
List comments on an ad

Returns comments on an ad's underlying creative post. Useful for moderating or analyzing engagement on dark posts (ad creatives that never went live organically), which the regular GET /v1/inbox/comments/{postId} endpoint cannot serve because dark posts are not in Zernio's post database.  Resolves the ad's creative effective_object_story_id (Facebook) or effective_instagram_media_id (Instagram) via the Marketing API on each call (cached in-process by the platform client), then fetches comments from the Graph API.  Meta-only. Other ad platforms (TikTok, LinkedIn, Pinterest, Google, X) do not expose a public per-ad comments API and return feature_not_available.  Requires the Ads add-on. Response shape matches GET /v1/inbox/comments/{postId}. 

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

