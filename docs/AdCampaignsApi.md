# \AdCampaignsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_ad_keywords**](AdCampaignsApi.md#add_ad_keywords) | **POST** /v1/ads/keywords | Add Search ad-group keywords
[**apply_google_recommendations**](AdCampaignsApi.md#apply_google_recommendations) | **POST** /v1/ads/recommendations/apply | Apply Google Ads recommendations
[**attach_ad_group_assets**](AdCampaignsApi.md#attach_ad_group_assets) | **POST** /v1/ads/ad-sets/{adSetId}/assets | Attach ad-group assets
[**attach_campaign_assets**](AdCampaignsApi.md#attach_campaign_assets) | **POST** /v1/ads/campaigns/{campaignId}/assets | Attach campaign assets
[**boost_post**](AdCampaignsApi.md#boost_post) | **POST** /v1/ads/boost | Boost post as ad
[**bulk_update_ad_campaign_status**](AdCampaignsApi.md#bulk_update_ad_campaign_status) | **POST** /v1/ads/campaigns/bulk-status | Pause or resume many campaigns
[**create_ad_campaign**](AdCampaignsApi.md#create_ad_campaign) | **POST** /v1/ads/campaigns | Create a standalone campaign
[**create_ad_set**](AdCampaignsApi.md#create_ad_set) | **POST** /v1/ads/ad-sets | Create a standalone ad group
[**create_bid_strategy**](AdCampaignsApi.md#create_bid_strategy) | **POST** /v1/ads/bid-strategies | Create portfolio bid strategy
[**create_google_asset_group**](AdCampaignsApi.md#create_google_asset_group) | **POST** /v1/ads/campaigns/{campaignId}/asset-groups | Create a Performance Max asset group
[**create_standalone_ad**](AdCampaignsApi.md#create_standalone_ad) | **POST** /v1/ads/create | Create standalone ad
[**delete_ad**](AdCampaignsApi.md#delete_ad) | **DELETE** /v1/ads/{adId} | Cancel an ad
[**delete_ad_campaign**](AdCampaignsApi.md#delete_ad_campaign) | **DELETE** /v1/ads/campaigns/{campaignId} | Delete a campaign
[**delete_ad_set**](AdCampaignsApi.md#delete_ad_set) | **DELETE** /v1/ads/ad-sets/{adSetId} | Delete an ad set
[**dismiss_google_recommendations**](AdCampaignsApi.md#dismiss_google_recommendations) | **POST** /v1/ads/recommendations/dismiss | Dismiss Google Ads recommendations
[**duplicate_ad**](AdCampaignsApi.md#duplicate_ad) | **POST** /v1/ads/{adId}/duplicate | Duplicate an ad
[**duplicate_ad_campaign**](AdCampaignsApi.md#duplicate_ad_campaign) | **POST** /v1/ads/campaigns/{campaignId}/duplicate | Duplicate a campaign
[**duplicate_ad_set**](AdCampaignsApi.md#duplicate_ad_set) | **POST** /v1/ads/ad-sets/{adSetId}/duplicate | Duplicate an ad set
[**edit_google_asset_group_assets**](AdCampaignsApi.md#edit_google_asset_group_assets) | **POST** /v1/ads/campaigns/{campaignId}/asset-groups/{assetGroupId}/assets | Link or unlink asset group assets
[**get_ad**](AdCampaignsApi.md#get_ad) | **GET** /v1/ads/{adId} | Get ad details
[**get_ad_campaign_details**](AdCampaignsApi.md#get_ad_campaign_details) | **GET** /v1/ads/campaigns/{campaignId} | Get live campaign details
[**get_ad_review**](AdCampaignsApi.md#get_ad_review) | **GET** /v1/ads/{adId}/review | Read the platform's review verdict for an ad
[**get_ad_set_details**](AdCampaignsApi.md#get_ad_set_details) | **GET** /v1/ads/ad-sets/{adSetId} | Get live ad-set details
[**get_ad_tree**](AdCampaignsApi.md#get_ad_tree) | **GET** /v1/ads/tree | Get campaign tree
[**get_ads_timeline**](AdCampaignsApi.md#get_ads_timeline) | **GET** /v1/ads/timeline | Get daily account metrics
[**get_campaign_ad_schedule**](AdCampaignsApi.md#get_campaign_ad_schedule) | **GET** /v1/ads/campaigns/{campaignId}/ad-schedule | Read a campaign's ad schedule (dayparting)
[**get_campaign_bidding**](AdCampaignsApi.md#get_campaign_bidding) | **GET** /v1/ads/campaigns/{campaignId}/bidding | Read a campaign's current bidding
[**get_campaign_conversion_goals**](AdCampaignsApi.md#get_campaign_conversion_goals) | **GET** /v1/ads/campaigns/{campaignId}/conversion-goals | Get campaign conversion goals
[**get_campaign_targeting**](AdCampaignsApi.md#get_campaign_targeting) | **GET** /v1/ads/campaigns/{campaignId}/targeting | Read a Google campaign's device, location, and language targeting
[**get_google_asset_group**](AdCampaignsApi.md#get_google_asset_group) | **GET** /v1/ads/campaigns/{campaignId}/asset-groups/{assetGroupId} | Get a Performance Max asset group
[**list_ad_campaigns**](AdCampaignsApi.md#list_ad_campaigns) | **GET** /v1/ads/campaigns | List campaigns
[**list_ad_group_assets**](AdCampaignsApi.md#list_ad_group_assets) | **GET** /v1/ads/ad-sets/{adSetId}/assets | List ad-group assets
[**list_ad_keywords**](AdCampaignsApi.md#list_ad_keywords) | **GET** /v1/ads/keywords | List Search keywords
[**list_ad_sets**](AdCampaignsApi.md#list_ad_sets) | **GET** /v1/ads/ad-sets | List ad sets
[**list_ads**](AdCampaignsApi.md#list_ads) | **GET** /v1/ads | List ads
[**list_bid_strategies**](AdCampaignsApi.md#list_bid_strategies) | **GET** /v1/ads/bid-strategies | List portfolio bid strategies
[**list_campaign_assets**](AdCampaignsApi.md#list_campaign_assets) | **GET** /v1/ads/campaigns/{campaignId}/assets | List campaign assets
[**list_campaign_negative_keyword_lists**](AdCampaignsApi.md#list_campaign_negative_keyword_lists) | **GET** /v1/ads/campaigns/{campaignId}/negative-keyword-lists | List campaign negative lists
[**list_campaign_negative_keywords**](AdCampaignsApi.md#list_campaign_negative_keywords) | **GET** /v1/ads/campaigns/{campaignId}/negative-keywords | List campaign-level negative keywords
[**list_google_asset_groups**](AdCampaignsApi.md#list_google_asset_groups) | **GET** /v1/ads/campaigns/{campaignId}/asset-groups | List Performance Max asset groups
[**list_google_recommendations**](AdCampaignsApi.md#list_google_recommendations) | **GET** /v1/ads/recommendations | List Google Ads recommendations
[**remove_ad_group_assets**](AdCampaignsApi.md#remove_ad_group_assets) | **DELETE** /v1/ads/ad-sets/{adSetId}/assets | Remove ad-group assets
[**remove_ad_keyword**](AdCampaignsApi.md#remove_ad_keyword) | **DELETE** /v1/ads/keywords/{keywordId} | Remove a Search keyword
[**remove_campaign_assets**](AdCampaignsApi.md#remove_campaign_assets) | **DELETE** /v1/ads/campaigns/{campaignId}/assets | Remove campaign assets
[**remove_google_asset_group**](AdCampaignsApi.md#remove_google_asset_group) | **DELETE** /v1/ads/campaigns/{campaignId}/asset-groups/{assetGroupId} | Remove a Performance Max asset group
[**replace_campaign_negative_keyword_lists**](AdCampaignsApi.md#replace_campaign_negative_keyword_lists) | **PUT** /v1/ads/campaigns/{campaignId}/negative-keyword-lists | Replace campaign negative lists
[**replace_campaign_negative_keywords**](AdCampaignsApi.md#replace_campaign_negative_keywords) | **PUT** /v1/ads/campaigns/{campaignId}/negative-keywords | Replace campaign-level negative keywords
[**replace_google_listing_group_filters**](AdCampaignsApi.md#replace_google_listing_group_filters) | **PUT** /v1/ads/campaigns/{campaignId}/asset-groups/{assetGroupId}/listing-group-filters | Replace an asset group's listing-group tree
[**update_ad**](AdCampaignsApi.md#update_ad) | **PUT** /v1/ads/{adId} | Update ad
[**update_ad_campaign**](AdCampaignsApi.md#update_ad_campaign) | **PUT** /v1/ads/campaigns/{campaignId} | Update a campaign
[**update_ad_campaign_status**](AdCampaignsApi.md#update_ad_campaign_status) | **PUT** /v1/ads/campaigns/{campaignId}/status | Pause or resume a campaign
[**update_ad_group_assets**](AdCampaignsApi.md#update_ad_group_assets) | **PUT** /v1/ads/ad-sets/{adSetId}/assets | Update ad-group assets
[**update_ad_keyword**](AdCampaignsApi.md#update_ad_keyword) | **PATCH** /v1/ads/keywords/{keywordId} | Pause or enable a Search keyword
[**update_ad_set**](AdCampaignsApi.md#update_ad_set) | **PUT** /v1/ads/ad-sets/{adSetId} | Update an ad set
[**update_ad_set_status**](AdCampaignsApi.md#update_ad_set_status) | **PUT** /v1/ads/ad-sets/{adSetId}/status | Pause or resume a single ad set
[**update_ad_status**](AdCampaignsApi.md#update_ad_status) | **PUT** /v1/ads/{adId}/status | Pause or resume a single ad
[**update_bid_strategy**](AdCampaignsApi.md#update_bid_strategy) | **PATCH** /v1/ads/bid-strategies/{strategyId} | Update portfolio bid strategy
[**update_campaign_ad_schedule**](AdCampaignsApi.md#update_campaign_ad_schedule) | **PUT** /v1/ads/campaigns/{campaignId}/ad-schedule | Replace a campaign's ad schedule (dayparting)
[**update_campaign_assets**](AdCampaignsApi.md#update_campaign_assets) | **PUT** /v1/ads/campaigns/{campaignId}/assets | Update campaign assets
[**update_campaign_conversion_goals**](AdCampaignsApi.md#update_campaign_conversion_goals) | **PATCH** /v1/ads/campaigns/{campaignId}/conversion-goals | Update campaign conversion goals
[**update_campaign_targeting**](AdCampaignsApi.md#update_campaign_targeting) | **PUT** /v1/ads/campaigns/{campaignId}/targeting | Edit a Google campaign's device, location, or language targeting
[**update_google_asset_group**](AdCampaignsApi.md#update_google_asset_group) | **PATCH** /v1/ads/campaigns/{campaignId}/asset-groups/{assetGroupId} | Update a Performance Max asset group



## add_ad_keywords

> models::AddAdKeywords201Response add_ad_keywords(add_ad_keywords_request)
Add Search ad-group keywords

Adds one or more keyword criteria to an existing Google Search ad group, without touching the keywords already there (unlike the whole-set diff on `PUT /v1/ads/{adId}`, `keywords`/`negativeKeywords` in `platformSpecificData`, which replaces the set). Set `negative: true` to add ad-group-level negatives instead of positive keywords. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**add_ad_keywords_request** | [**AddAdKeywordsRequest**](AddAdKeywordsRequest.md) |  | [required] |

### Return type

[**models::AddAdKeywords201Response**](addAdKeywords_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## apply_google_recommendations

> models::ApplyGoogleRecommendations200Response apply_google_recommendations(apply_google_recommendations_request)
Apply Google Ads recommendations

Apply up to 100 recommendations. This changes the account (budgets, bidding, keywords, assets) and is not reversible or idempotent; Google offers no validate-only mode for it. Items run in partial-failure mode, so one stale recommendation does not block the rest. `parameters` is optional and takes exactly one key named for the recommendation type, in Google's ApplyRecommendationOperation shape (for example `campaignBudget: { newBudgetAmountMicros }` or `keyword: { matchType, cpcBidMicros }`); omit it to apply Google's suggested values.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**apply_google_recommendations_request** | [**ApplyGoogleRecommendationsRequest**](ApplyGoogleRecommendationsRequest.md) |  | [required] |

### Return type

[**models::ApplyGoogleRecommendations200Response**](applyGoogleRecommendations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## attach_ad_group_assets

> models::AttachAdGroupAssets201Response attach_ad_group_assets(ad_set_id, attach_campaign_assets_request)
Attach ad-group assets

Creates and attaches sitelinks, callouts and structured snippets in one Google mutation.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_set_id** | **String** | Numeric Google platform id. | [required] |
**attach_campaign_assets_request** | [**AttachCampaignAssetsRequest**](AttachCampaignAssetsRequest.md) |  | [required] |

### Return type

[**models::AttachAdGroupAssets201Response**](attachAdGroupAssets_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## attach_campaign_assets

> models::AttachCampaignAssets201Response attach_campaign_assets(campaign_id, attach_campaign_assets_request)
Attach campaign assets

Creates and attaches sitelinks, callouts and structured snippets in one Google mutation.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Numeric Google platform id. | [required] |
**attach_campaign_assets_request** | [**AttachCampaignAssetsRequest**](AttachCampaignAssetsRequest.md) |  | [required] |

### Return type

[**models::AttachCampaignAssets201Response**](attachCampaignAssets_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## boost_post

> models::UpdateAd200Response boost_post(boost_post_request, idempotency_key)
Boost post as ad

Creates a paid ad from an existing published post, keeping the post's engagement. By default it provisions the whole hierarchy (campaign, ad set, ad).  **Attach shape (Meta).** Send `adSetId` to put the ad under an EXISTING ad set instead, so that ad set keeps its learning phase. It then owns `budget`, `schedule` and `targeting`, and sending any of those alongside `adSetId` is a 400 rather than a silent drop. `budget` is required only without `adSetId`.  `instagramAccountId`, `destinationType`, `whatsappPhoneNumber` and `adSetId` are Meta-only and return 400 on other platforms.  `accountId` may be a Facebook, Instagram or Meta ads (business login) connection. A business-login connection has no posting account, so pass the post as `platformPostId` (Facebook `pageId_postId` or an Instagram media id); a Zernio `postId` is a 400 there.  **Messaging boosts (Meta).** Use `goal: engagement` with `callToAction: WHATSAPP_MESSAGE`, `MESSAGE_PAGE`, or `INSTAGRAM_MESSAGE`. The CTA implies WHATSAPP, MESSENGER, or INSTAGRAM_DIRECT respectively; `destinationType` alone does not select a messaging CTA. Omit `linkUrl` only for messaging CTAs. Plain link CTAs keep their goal and link behavior when combined with an independent `destinationType`. The campaign uses OUTCOME_ENGAGEMENT and the ad set uses CONVERSATIONS with the promoted Page. Optional `whatsappPhoneNumber` selects a number already paired with that Page. Conflicting CTA/destination, instant form, goal, or optimizationGoal inputs return 400. Attach requires the target ad set destination to match. Existing post references preserve social proof; an Instagram reel rejected by Meta is not re-uploaded as a new post for a messaging boost.  **Retries.** Boosts are NOT idempotent and can take minutes when Meta requires re-hosting an Instagram video, so do not retry on client timeout. Send an Idempotency-Key header to make retries safe: same key and body replays the original 201, and distinct keys always create distinct ads. Without the header, an identical request is treated as a retry: while one is in flight it returns 409, and within 10 minutes of a completed boost it returns the already-created ad instead of creating another. To intentionally duplicate an ad, send distinct Idempotency-Keys (or vary the body, e.g. the name). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**boost_post_request** | [**BoostPostRequest**](BoostPostRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. |  |

### Return type

[**models::UpdateAd200Response**](updateAd_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## bulk_update_ad_campaign_status

> models::BulkUpdateAdCampaignStatus200Response bulk_update_ad_campaign_status(bulk_update_ad_campaign_status_request)
Pause or resume many campaigns

Process up to 50 campaigns in one call. Each campaign is updated concurrently and the response contains a per-campaign result so a single bad row does not fail the whole batch. Each campaign is read, written and re-read exactly as PUT /v1/ads/campaigns/{campaignId}/status describes: only the campaign's own switch is written, never its ad sets' or ads'. `updated` / `skipped` count campaigns. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**bulk_update_ad_campaign_status_request** | [**BulkUpdateAdCampaignStatusRequest**](BulkUpdateAdCampaignStatusRequest.md) |  | [required] |

### Return type

[**models::BulkUpdateAdCampaignStatus200Response**](bulkUpdateAdCampaignStatus_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_ad_campaign

> models::CreateAdCampaign200Response create_ad_campaign(create_ad_campaign_request, idempotency_key)
Create a standalone campaign

Creates a campaign WITHOUT its first ad set / ad, on the platform of the given `accountId`. Ad sets join it later via `existingCampaignId` on the create endpoints. Platform notes: on Meta a budget here is campaign-level (CBO) by definition; omit it for ABO (each ad set carries its own budget), and `specialAdCategories` is Meta-only (400 elsewhere); `bidStrategy` is Meta and Google (400 elsewhere), and Google also accepts `portfolioBidStrategyId` instead. Google, X and OpenAI require a budget (422 without one; OpenAI accepts daily or lifetime, Google only `budgetType: daily`). On OpenAI `goal` sets the campaign objective, and `conversions` needs an active standard conversion event on the account. LinkedIn creates the campaign GROUP (our campaign level) and rejects a budget, which lives on the campaign (ad set) level there; it comes back `status: DRAFT`. Created `PAUSED` (TikTok `DISABLE`) unless `status: ACTIVE` where the platform supports it.  **Idempotency:** send an `Idempotency-Key` header to make retries safe.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_ad_campaign_request** | [**CreateAdCampaignRequest**](CreateAdCampaignRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. Only 2xx responses are stored, so a request that failed with a 4xx can be retried with a corrected body under the SAME key. |  |

### Return type

[**models::CreateAdCampaign200Response**](createAdCampaign_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_ad_set

> models::CreateAdSet201Response create_ad_set(create_ad_set_request, idempotency_key)
Create a standalone ad group

Google Ads compliance row C.190: creates an ad group WITHOUT an ad, under an existing campaign. Ads join it later via `adSetId` on POST /v1/ads/create. Google only; every other platform returns 501.  Created `PAUSED` unless `status: ACTIVE`. The new ad group has no ad yet, so it will not appear in GET /v1/ads/tree (built purely from `ads` rows) until one is added; use GET /v1/ads/ad-sets to see it in the meantime.  **Idempotency:** send an `Idempotency-Key` header to make retries safe.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_ad_set_request** | [**CreateAdSetRequest**](CreateAdSetRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. Only 2xx responses are stored, so a request that failed with a 4xx can be retried with a corrected body under the SAME key. |  |

### Return type

[**models::CreateAdSet201Response**](createAdSet_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_bid_strategy

> models::CreateBidStrategy201Response create_bid_strategy(create_bid_strategy_request)
Create portfolio bid strategy

Creates a standalone bid strategy shared across campaigns. Attach it to a campaign with `portfolioBidStrategyId` on POST /v1/ads/create, PUT /v1/ads/campaigns/{campaignId}, or PUT /v1/ads/ad-sets/{adSetId}. Attaching a strategy aligned to a shared budget fails there with a 400 (Google's `BIDDING_STRATEGY_AND_BUDGET_MUST_BE_ALIGNED`); this is not retryable.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_bid_strategy_request** | [**CreateBidStrategyRequest**](CreateBidStrategyRequest.md) |  | [required] |

### Return type

[**models::CreateBidStrategy201Response**](createBidStrategy_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_google_asset_group

> models::CreateGoogleAssetGroup200Response create_google_asset_group(campaign_id, create_google_asset_group_request)
Create a Performance Max asset group

Add an asset group to an existing Performance Max campaign. The group, any new assets, their links and an optional listing-group tree are created in one atomic request, so Google checks the asset minimums (for non-retail campaigns) against the whole set. Created PAUSED unless status is ENABLED. validateOnly: true runs Google's validation without creating anything.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Google Ads campaign id. | [required] |
**create_google_asset_group_request** | [**CreateGoogleAssetGroupRequest**](CreateGoogleAssetGroupRequest.md) |  | [required] |

### Return type

[**models::CreateGoogleAssetGroup200Response**](createGoogleAssetGroup_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_standalone_ad

> models::CreateStandaloneAd200Response create_standalone_ad(create_standalone_ad_request, idempotency_key)
Create standalone ad

Create a paid ad with custom creative across Meta, Google Ads, Pinterest, TikTok, X, LinkedIn, and OpenAI Ads (ChatGPT Ads).  Google Performance Max: set `campaignType: \"pmax\"` and supply `assetGroup` with text, images by role, business name and finalUrl. Creates a daily budget, PAUSED campaign and asset group atomically. `validateOnly: true` validates the complete request with Google without creating or persisting resources. Read assets with `GET /v1/ads/campaigns/{campaignId}/asset-groups`. The logo is required; video is optional via `assetGroup.youtubeVideoId`. Brand guidelines are disabled at creation. All supplied asset links are validated together against Google's minimum asset requirements. PMax rejects ACTIVE creation, portfolio bidding, bid caps, legacy creative fields and attach shapes. Geo and language targeting are supported; omitted geo targets all locations. PMax does not require top-level goal, headline, body or linkUrl. Supported bidding: omitted or LOWEST_COST_WITHOUT_CAP for Maximize Conversions, COST_CAP plus bidAmount for target CPA, LOWEST_COST_WITH_MIN_ROAS plus roasAverageFloor for Maximize Conversion Value with target ROAS.  Google Demand Gen: set `campaignType: \"demand_gen\"` and supply `demandGen`. Creates a daily budget, PAUSED campaign, one ad group and one ad in a single atomic request: a multi-asset image ad, a video responsive ad when `demandGen.youtubeVideoIds` is sent, or a carousel ad (2 to 10 cards) when `demandGen.carouselCards` is sent. Geo (countries, regions, cities, zips, metros) and languages go on the ad group, as Demand Gen requires. `demandGen.channels` sets the ad group's channel controls and `demandGen.audience` builds a Google Audience (user lists, interests, custom audiences, age ranges, genders) attached to the ad group, or `demandGen.audienceId` attaches an existing one. `validateOnly: true` validates everything with Google without creating resources. Supported bidding: omitted or LOWEST_COST_WITHOUT_CAP for Maximize Conversions, COST_CAP plus bidAmount for target CPA, LOWEST_COST_WITH_MIN_ROAS plus roasAverageFloor for target ROAS, LOWEST_COST_WITH_BID_CAP plus bidAmount for target CPC. The created ad carries the native `platformCampaignId`, `platformAdSetId` (ad group) and `platformAdId`. Activate with PUT /v1/ads/campaigns/{campaignId}/status; budget, bidding and name are edited with the regular campaign endpoints; creative, channels, audience and ad group targeting with PUT /v1/ads/{adId} (`demandGen`, `targeting`). To grow an existing Demand Gen campaign, send `existingCampaignId` (adds a PAUSED ad group, with its own geo, languages, channels and audience, plus its ad) or `adSetId` (adds a PAUSED ad to that ad group); neither takes budget, bidding or schedule fields, and both support `validateOnly`.  Other mutually-exclusive request shapes are selected by the body:  - Legacy single-creative shape (all platforms, the default). - Meta-only multi-creative shape via the creatives array: one ad set with N ads sharing budget and targeting. - Attach shape via adSetId: adds one new ad to an existing ad set, inheriting its budget, targeting, and schedule (Meta, Google Ads, TikTok, and LinkedIn). On LinkedIn adSetId is the existing Campaign id, and the budget, schedule, targeting and bidding fields must be omitted. On LinkedIn `goal` may be omitted too (taken from the Campaign's objective), and the created ad's `targeting` echoes the Campaign's audience.  Meta accepts `creativeFeatures` on the single and attach shapes and as defaults for `creatives[]`; an item replaces the whole feature map. `promotion` is not supported on any shape and any object is rejected with 400. Reusing `existingCreativeId` uses the existing creative settings instead of new settings. Requested settings are persisted for lists, exports, and default ad-detail reads.  Per-platform required fields, budget minimums, and video-ad rules are documented on each property below.  LinkedIn creates a Single Image or Single Video Ad backed by a Direct Sponsored Content \"dark post\" authored by a Company Page (see `organizationId`). Supported goals are engagement, traffic, awareness, and video_views (video ads use the `video` field; video_views requires a video), and traffic ads require `linkUrl`.  **Idempotency:** this endpoint is not idempotent at the platform level (a blind retry creates a second campaign/ad set/ad). Send an `Idempotency-Key` header to make retries safe: the first request with a given key creates the ad and we store the response; a retry with the same key replays that exact response (with `Idempotent-Replayed: true`) instead of creating duplicates. Reusing a key with a different body returns 422; a key whose first request is still in flight returns 409 (retry after a short backoff). Keys are scoped to your credential and expire after 24h. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_standalone_ad_request** | [**CreateStandaloneAdRequest**](CreateStandaloneAdRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. |  |

### Return type

[**models::CreateStandaloneAd200Response**](createStandaloneAd_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_ad

> models::DeleteAccountGroup200Response delete_ad(ad_id)
Cancel an ad

Deletes the ad on the platform and marks it as cancelled in the database. The ad is preserved for history. OpenAI Ads has no delete API; the ad is archived instead (a terminal state, the closest equivalent).  Only the ad is deleted; a campaign or ad set is never deleted while it still holds another ad. On Meta, when the ad set and campaign were created by Zernio (by `POST /v1/ads/create` or `POST /v1/ads/boost`) and Meta lists no other ad in the ad set (archived ads count), the emptied ad set is deleted too, then the campaign once it holds no other ad set. Parents created outside Zernio, and the parents of an ad imported from the platform, are always kept. On LinkedIn the ad is a creative inside a campaign inside a campaign group: the creative is always removed, the campaign only when Zernio created it and LinkedIn lists no other creative in it that is not archived, canceled or deleted, and the campaign group only when Zernio created it and LinkedIn lists no other campaign in it that is not canceled or deleted (archived campaigns count). If the creative itself cannot be removed the request fails and no parent is touched. To delete a whole campaign on purpose use `DELETE /v1/ads/campaigns/{campaignId}`. 

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


## delete_ad_campaign

> models::DeleteAdCampaign200Response delete_ad_campaign(campaign_id, delete_ad_campaign_request)
Delete a campaign

Deletes the whole campaign on the platform, cascading to its ad sets and ads. Locally, all Ad documents for this campaign are marked `status: cancelled`.  **Empty campaigns.** A campaign with zero ads has no local Ad documents to resolve, so it is invisible to `/v1/ads/tree` and this endpoint would 404. That state is produced by the two-step create flow (campaign, then ads via `existingCampaignId`) whenever Meta rejects the ad step. To delete such a shell, send `accountId` in the body: we skip the local lookup entirely and forward the delete to Meta. `accountId` is ignored when the campaign does have ads. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Platform campaign ID | [required] |
**delete_ad_campaign_request** | [**DeleteAdCampaignRequest**](DeleteAdCampaignRequest.md) |  | [required] |

### Return type

[**models::DeleteAdCampaign200Response**](deleteAdCampaign_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_ad_set

> models::DeleteAdSet200Response delete_ad_set(ad_set_id)
Delete an ad set

Deletes the ad set on the platform, cascading to its ads only (never the campaign). Locally, every Ad document under the ad set is marked `status: cancelled`.  Delete is soft on platforms that have no hard delete: LinkedIn moves the campaign to `PENDING_DELETION`, Pinterest archives the ad group, and X soft-flags the line item. Google removes the ad group. All remain readable for reporting. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_set_id** | **String** | Platform ad set ID | [required] |

### Return type

[**models::DeleteAdSet200Response**](deleteAdSet_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## dismiss_google_recommendations

> models::ApplyGoogleRecommendations200Response dismiss_google_recommendations(dismiss_google_recommendations_request)
Dismiss Google Ads recommendations

Dismiss up to 100 recommendations so Google stops suggesting them. Items run in partial-failure mode.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**dismiss_google_recommendations_request** | [**DismissGoogleRecommendationsRequest**](DismissGoogleRecommendationsRequest.md) |  | [required] |

### Return type

[**models::ApplyGoogleRecommendations200Response**](applyGoogleRecommendations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## duplicate_ad

> models::DuplicateAd200Response duplicate_ad(ad_id, idempotency_key, duplicate_ad_request)
Duplicate an ad

Duplicates a single ad via Meta's native `POST /{ad-id}/copies`. The copy is created paused. `adSetId` retargets the copy into another ad set; omitted = the source's own ad set. Accepts the Zernio ad id or the platform ad id. Sync discovery is triggered automatically (`syncAfter: false` to skip). Creative settings returned by Meta, including explicit promotion metadata and creativeFeatures, are preserved when the native copy requires a creative rebuild. Metadata Meta does not return cannot be recovered. When Meta refuses the native copy with its capability error (code 3), which happens for some creatives built by other tools, the ad is rebuilt instead: a new creative from the source's returned spec and a new ad in the target ad set, carrying the source name, status option, rename options and tracking specs.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_id** | **String** | Zernio ad ID or platform ad ID | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. Only 2xx responses are stored, so a request that failed with a 4xx can be retried with a corrected body under the SAME key. |  |
**duplicate_ad_request** | Option<[**DuplicateAdRequest**](DuplicateAdRequest.md)> |  |  |

### Return type

[**models::DuplicateAd200Response**](duplicateAd_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## duplicate_ad_campaign

> models::DuplicateAdCampaign200Response duplicate_ad_campaign(campaign_id, duplicate_ad_campaign_request, idempotency_key)
Duplicate a campaign

Duplicates a campaign, including its ad sets, ads, creatives, and targeting by default (`deepCopy: true`). The copy is created paused so callers can review before launching.  Per-platform implementation: - **Meta** uses the native `POST /{campaign-id}/copies` endpoint. - **TikTok** has no native copy primitive; Zernio walks the source   graph (`/v2/campaign/get/`, `/v2/adgroup/get/`, `/v2/ad/get/`) and   recreates each entity via the corresponding `/create/` endpoints,   carrying over budget / targeting / bid_type / bid_price /   deep_bid_type / creative fields. Spark Ad linkage (`tiktok_item_id`)   is preserved. - **LinkedIn** has no native copy primitive; Zernio walks the source   CampaignGroup → Campaigns → Creatives and recreates each entity,   carrying over `type` / `costType` / `unitCost` /   `optimizationTargetType` / `creativeSelection` / `objectiveType` /   `format` / `dailyBudget` / `totalBudget` / `targetingCriteria` /   `runSchedule` and every Creative's `content` object verbatim.   `statusOption: INHERITED_FROM_SOURCE` is evaluated **per entity**:   any Group / Campaign / Creative whose source is `ACTIVE` gets its   clone activated too. Duplicating an ACTIVE campaign with   `INHERITED_FROM_SOURCE` starts a second front of spend the moment   the clone activates. The safe default is `PAUSED`.  The new hierarchy is asynchronous to materialize in our DB, and we trigger sync discovery automatically. Set `syncAfter: false` to skip and poll `/v1/ads/tree` on your own cadence.  Other platforms return 501 Not Implemented. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Source platform campaign ID | [required] |
**duplicate_ad_campaign_request** | [**DuplicateAdCampaignRequest**](DuplicateAdCampaignRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. Only 2xx responses are stored, so a request that failed with a 4xx can be retried with a corrected body under the SAME key. |  |

### Return type

[**models::DuplicateAdCampaign200Response**](duplicateAdCampaign_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## duplicate_ad_set

> models::DuplicateAdSet200Response duplicate_ad_set(ad_set_id, duplicate_ad_set_request, idempotency_key)
Duplicate an ad set

Duplicates an ad set. The copy is created paused so callers can review before launching. `campaignId` retargets the copy into another campaign; omitted = the source's own campaign.  Meta: ads and creatives are included by default (`deepCopy: true`) via Meta's native `POST /{adset-id}/copies`; the new hierarchy materializes asynchronously and sync discovery is triggered automatically (`syncAfter: false` to skip).  TikTok: the ad group is read and recreated under the campaign with its targeting, bidding, budget and schedule (start reset to now); `deepCopy: true` recreates its ads too (default false). `startTime`, `endTime` and `renameStrategy` are ignored and `statusOption` must be PAUSED or absent. The copy appears on the next discovery sync.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_set_id** | **String** | Source platform ad set ID | [required] |
**duplicate_ad_set_request** | [**DuplicateAdSetRequest**](DuplicateAdSetRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. Only 2xx responses are stored, so a request that failed with a 4xx can be retried with a corrected body under the SAME key. |  |

### Return type

[**models::DuplicateAdSet200Response**](duplicateAdSet_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## edit_google_asset_group_assets

> models::EditGoogleAssetGroupAssets200Response edit_google_asset_group_assets(campaign_id, asset_group_id, edit_google_asset_group_assets_request)
Link or unlink asset group assets

Link existing assets or new content to the asset group, and unlink assets, in one atomic request. Links are applied before unlinks, so swapping the last asset of a role does not trip Google's per-role minimum. Unlinking removes the link only; the asset stays in the account library. validateOnly: true validates without writing.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Google Ads campaign id. | [required] |
**asset_group_id** | **String** | Google asset group id. | [required] |
**edit_google_asset_group_assets_request** | [**EditGoogleAssetGroupAssetsRequest**](EditGoogleAssetGroupAssetsRequest.md) |  | [required] |

### Return type

[**models::EditGoogleAssetGroupAssets200Response**](editGoogleAssetGroupAssets_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad

> models::GetAd200Response get_ad(ad_id, live)
Get ad details

Returns an ad with its creative, targeting, status, and performance metrics. Google Search ads include current creative.headlines, creative.descriptions and creative.finalUrls, preserving pinnedField. Top-level cachedAt and stale report cache freshness. Google mutations invalidate this read. RSA enrichment requires a stored advertisingChannelType of SEARCH. Ads with an unknown or other channel return their stored details without a Google read. If RSA enrichment fails, the stored ad is returned with HTTP 200 and without cache metadata.  The `{adId}` path segment accepts any identifier dialect Zernio indexes for the ad: - the Zernio internal `_id` (24-char hex) - Meta's numeric `platformAdId` (the value shipped in `comment.received` webhooks as `comment.ad.id`) - the creative's `effective_object_story_id` (`{pageId}_{postId}` shape, Facebook side) - the creative's `effective_instagram_media_id` (Instagram side)  Any of the four resolve to the same ad. Caller doesn't need a translation step. `creative.creativeFeatures` holds the stored requested settings, which do not confirm platform application.  **Status freshness.** `status`, `configuredStatus`, `platformStatus`, `platformAdSetStatus` and `platformCampaignStatus` are the values Zernio last stored. Background sync refreshes them, typically within 15 to 60 minutes (Google up to about 3 hours), and ended or long-paused objects may be refreshed less often. Zernio's own status writes re-read the switches they change. A change made in the platform's own ads manager therefore shows up here only after the next sync. Controllers that act on a switch should pass `live=true`, which reads the switches from the platform now, stores them, and returns `statusReadAt` (null when the read failed and the stored values were returned). With `live=true` the ad's own switch (`configuredStatus`), its delivery status (`status`, `platformStatus`) and its ad set and campaign switches (`platformAdSetStatus`, `platformCampaignStatus`) are read live. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_id** | **String** | Zernio `_id` (hex), Meta `platformAdId` (numeric), or one of the creative's effective story/media IDs. See description for details.  | [required] |
**live** | Option<**bool**> | Read the on/off switches live from the platform instead of returning the synced values. The fresh values are stored (so later reads return them too) and the response carries `statusReadAt`, the time of the read. At most 20 platform objects are read per request. Where a read fails (credentials, platform error, no reader on that platform), the stored values come back with `statusReadAt: null`. See \"Status freshness\" in the operation description. |  |[default to false]

### Return type

[**models::GetAd200Response**](getAd_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad_campaign_details

> models::GetAdCampaignDetails200Response get_ad_campaign_details(campaign_id, account_id, fields)
Get live campaign details

Reads one campaign live from Meta, returned verbatim, so a caller that knows a campaign id no longer has to page `GET /v1/ads/campaigns` to find it. The default projection covers name, status, objective, buying type, bid strategy, budgets, spend cap, schedule and `issues_info`. `fields` is a raw-passthrough override; unknown fields return Meta's 400 verbatim. A campaign the resolved connection cannot see comes back as Meta's own 400, not a 404.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Meta campaign id (platformCampaignId). | [required] |
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. | [required] |
**fields** | Option<**String**> | Comma-separated Graph field override. Supports nested {} projections and Graph field modifiers. |  |

### Return type

[**models::GetAdCampaignDetails200Response**](getAdCampaignDetails_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad_review

> models::GetAdReview200Response get_ad_review(ad_id)
Read the platform's review verdict for an ad

Reads the ad's review verdict from the platform now: whether it was approved, where it may not deliver, and every rejection reason with TikTok's suggestion and the piece of content it refers to. Read-only, so it works on a paused ad without re-enabling it.  TikTok only (`/ad/review_info/`); every other platform returns 501. Use it alongside the ad's `platformStatus`: TikTok reports `AD_STATUS_AUDIT` while the ad is in review and `AD_STATUS_AD_PRE_ONLINE` once it passed and is about to deliver (both map to `status: pending_review`); `AD_STATUS_AUDIT_DENY` maps to `rejected`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_id** | **String** | Zernio ad id (24-char hex) or the platform ad id. | [required] |

### Return type

[**models::GetAdReview200Response**](getAdReview_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad_set_details

> models::GetAdSetDetails200Response get_ad_set_details(ad_set_id, account_id, fields)
Get live ad-set details

Reads the ad set live from Meta, returned verbatim. The default projection includes `learning_stage_info` (learning-phase status: LEARNING / SUCCESS / FAIL / WAIVING; Meta omits its `status` key on paused ad sets), delivery settings, budgets, schedule and targeting. `fields` is a raw-passthrough override; unknown fields return Meta's 400 verbatim.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_set_id** | **String** | Meta ad set id (platformAdSetId). | [required] |
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. | [required] |
**fields** | Option<**String**> | Comma-separated Graph field override. Supports nested {} projections and Graph field modifiers, so a nested edge can be paged explicitly: without a .limit() modifier the expansion runs at the Meta default page size and the tail is dropped silently. |  |

### Return type

[**models::GetAdSetDetails200Response**](getAdSetDetails_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad_tree

> models::AdTreeResponse get_ad_tree(page, limit, source, platform, status, ad_account_id, page_id, account_id, profile_id, campaign_id, updated_since, search, from_date, to_date, has_delivery, min_spend, sort, time_increment, daily_level)
Get campaign tree

Returns a nested Campaign > Ad Set > Ad hierarchy with rolled-up metrics at each level. Uses a two-stage aggregation: ads are grouped into ad sets, then ad sets into campaigns. Metrics are computed over an optional date range, then rolled up from ad level to ad set and campaign levels. Pagination is at the campaign level. Ads without a campaign or ad set ID are grouped into synthetic \"Ungrouped\" buckets. If no date range is provided, defaults to the last 90 days. Date range is capped at 730 days max.  Pass `timeIncrement=1` to also get a daily breakdown: each node gains a `daily[]` array of per-day metrics (same fields as the aggregated `metrics`) in the same call. Use `dailyLevel` (`campaign` default, or `adset` / `ad`) to choose which levels carry the series. This replaces calling the tree once per day for per-campaign daily trends.  **Deleted objects stay in the tree.** Deleting an ad or a campaign is a soft delete: the Ad documents move to `status: cancelled` and are kept indefinitely, so their historical spend still counts toward the metrics of any date range they fall in. There is no pruning job and no retention window. Filter on `status` if your view should hide them, but do that after reading the totals, not before. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**page** | Option<**i32**> | Page number (1-based) |  |[default to 1]
**limit** | Option<**i32**> | Campaigns per page |  |[default to 20]
**source** | Option<**String**> | `all` (default) returns both Zernio-created ads and those discovered from the platform's ad manager. Matches the web UI's default view. Pass `zernio` to restrict to isExternal=false only. Status is NOT filtered by default; use the `status` param for that. |  |[default to all]
**platform** | Option<**String**> |  |  |
**status** | Option<[**AdStatus**](AdStatus.md)> | Filter by derived campaign status (post-aggregation) |  |
**ad_account_id** | Option<**String**> | One or more platform ad account IDs to scope the tree to (agency profiles connect a whole Business Manager but a team usually cares about a subset). Comma-separate for multiple (`?adAccountId=act_1,act_2,act_3`); single value keeps its old shape. Max 50 accounts per request; the plural aliases `adAccountIds` and `platformAdAccountIds` are rejected with a 400 to stop them from silently returning the unfiltered fleet. |  |
**page_id** | Option<**String**> | Meta only: Facebook Page ID. Prunes the tree to ads whose creative is backed by this Page: campaigns and ad sets with no ad on the Page drop out, and rolled-up metrics cover only the Page's ads. Mirrors the same filter on /v1/ads and /v1/ads/campaigns. |  |
**account_id** | Option<**String**> | Account ID |  |
**profile_id** | Option<**String**> | Profile ID |  |
**campaign_id** | Option<**String**> | Restrict the tree to one or more campaigns by platform campaign id (the id the platform assigns, e.g. Meta's numeric campaign id). Comma-separate up to 100 ids (`?campaignId=123,456`). Filters the campaign set itself, so it works regardless of account size and pagination. Pass this when you already hold campaign ids (for example from an `ad.status_changed` webhook) instead of paging the whole tree. |  |
**updated_since** | Option<**String**> | Return only campaigns with a change stored since this time (ISO 8601 with offset, e.g. `2026-09-30T10:00:00Z`): a new ad, or a change to any ad's status, review status, name, budget or creative. Each matching campaign comes back whole (every ad set and ad). Metrics are not a change: to refresh numbers, filter with `hasDelivery=true` and a date range instead. Combines with every other filter (with `hasDelivery`/`minSpend` a campaign must match both). |  |
**search** | Option<**String**> | Case-insensitive substring match on campaign, ad set and ad names (`_`, `%` and spaces match literally), or an exact platform campaign, ad set or ad id. A campaign whose name matches returns with all its ad sets and ads; a match on an ad set or ad name returns only the matching branch. Filters the campaign set itself, so `pagination.total` counts only matching campaigns. |  |
**from_date** | Option<**String**> | Start of the METRICS date range (YYYY-MM-DD). On its own it affects only the spend/impression numbers overlaid on each node, not which campaigns are returned. Pass `hasDelivery` or `minSpend` to also filter the campaign set to this window. Defaults to 90 days ago. |  |
**to_date** | Option<**String**> | End of metrics date range (YYYY-MM-DD). Defaults to today. Max 730-day range. |  |
**has_delivery** | Option<**bool**> | Return only campaigns that delivered between `fromDate` and `toDate`: spend above zero, or impressions served at zero spend. Unlike `status`, which reads a campaign's CURRENT state, this filters on what happened inside the window, so a campaign that spent then and is paused today is still returned. Filters the campaign set itself, so `pagination.total` counts only matching campaigns. |  |
**min_spend** | Option<**f64**> | Return only campaigns whose spend between `fromDate` and `toDate` reaches this amount. Expressed in each campaign's OWN currency (the `currency` field on the campaign node): spend is stored per ad account in its native currency and one response can span several. Implies `hasDelivery`; `minSpend=0` applies no filter. |  |
**sort** | Option<**String**> | Campaign-level sort order. `newest` (default) / `oldest` order by the campaign's newest-ad createdAt. `spend_desc` / `spend_asc` order by aggregated spend in the requested date range; campaigns with no spend land at the end. |  |[default to newest]
**time_increment** | Option<**i32**> | Set to `1` to also return a daily breakdown. Mirrors Meta Insights' `time_increment=1`: each node gains a `daily[]` array of per-day metrics (same fields as the aggregated `metrics`) alongside the range total, so you get per-entity daily trends in ONE call instead of calling the tree once per day. Only `1` (daily) is supported. The daily series covers the same date range and uses the same source data as `metrics`, except `reach` on Meta and TikTok: the range total is the platform's de-duplicated value, so daily reach does not sum to it. See `dailyLevel` to control which levels carry it. |  |
**daily_level** | Option<**String**> | Which tree levels get the `daily[]` series when `timeIncrement=1`. `campaign` (default) attaches it on campaign nodes only: the common per-campaign-trend case, and the smallest payload. `adset` adds it on ad sets too; `ad` adds it on every ad in `ads[]` as well (heaviest: a long range × up to 100 ads per ad set). Scope with `campaignId` to keep `ad`-level responses small. Ignored when `timeIncrement` is unset. |  |[default to campaign]

### Return type

[**models::AdTreeResponse**](AdTreeResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ads_timeline

> models::AdsTimelineResponse get_ads_timeline(account_id, ad_account_id, from_date, to_date, platform)
Get daily account metrics

Returns daily aggregate metrics across all ads in a SocialAccount as a single time series, one row per calendar day in the requested range. Use this for dashboards that draw a daily-spend or daily-conversions chart, instead of calling `/v1/ads/tree` once per day.  `accountId` is required. The lookup is sibling-expanded so passing the `metaads` ID also includes ads under the linked `facebook` / `instagram` posting account (and vice-versa), the same convention as `/v1/ads/tree` and `/v1/ads`.  Date range defaults to the last 90 days. Capped at 730 days. Ranges older than the ingested history return a `202` immediately with the covered part and `backfillPending: true` while the rest is backfilled in the background; repeat the request shortly until it returns 200 with full data.  With adAccountId set to a Google customer id this is the customer-level performance report (clicks, cost, impressions, conversions, all conversions per day). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Account ID. Sibling-expanded to its linked posting↔ads pair. | [required] |
**ad_account_id** | Option<**String**> | Optional platform-native ad account ID (e.g. Meta `act_…`, TikTok advertiser ID). Use when the connection wraps multiple platform ad accounts and the chart should show one only. Note: rows ingested before 2026-05-13 don't carry this column; the recurring 7-day re-sync repopulates them naturally. |  |
**from_date** | Option<**String**> | Inclusive start of metrics range (YYYY-MM-DD). Defaults to 90 days ago. |  |
**to_date** | Option<**String**> | Inclusive end of metrics range (YYYY-MM-DD). Defaults to today. Max 730-day range. |  |
**platform** | Option<**String**> | Restrict to one platform. |  |

### Return type

[**models::AdsTimelineResponse**](AdsTimelineResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_campaign_ad_schedule

> models::GetCampaignAdSchedule200Response get_campaign_ad_schedule(campaign_id, platform, include_performance, window_days, from_date, to_date)
Read a campaign's ad schedule (dayparting)

The windows a Google campaign serves in, with the bid modifier on each, plus the criterion ids Google minted for them.  An EMPTY `schedule` is meaningful and is not a failed lookup: Google has no \"all day\" criterion, so a campaign with no ad schedule serves around the clock. `servesAroundTheClock` states that explicitly.  Set `includePerformance=true` to also get delivery split by day of week and by hour, which is the evidence for deciding what the schedule should be. It is one extra Google call segmented by both dimensions at once, so the two views always agree.  Google Ads only. The response carries `cachedAt` and `stale`, set when a quota-exhausted call falls back to the last-good copy instead of a live read. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Numeric Google platform campaign id. | [required] |
**platform** | Option<**String**> | Disambiguates the campaign id when the connection spans platforms. |  |
**include_performance** | Option<**bool**> | Also return delivery by day of week and by hour. Costs one extra Google call. |  |
**window_days** | Option<**i32**> | Trailing window for the performance split. Ignored when fromDate and toDate are both given. |  |[default to 30]
**from_date** | Option<**String**> | Start of an explicit performance range (YYYY-MM-DD). Use together with toDate. |  |
**to_date** | Option<**String**> | End of an explicit performance range (YYYY-MM-DD). Must be on or after fromDate. |  |

### Return type

[**models::GetCampaignAdSchedule200Response**](getCampaignAdSchedule_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_campaign_bidding

> models::GetCampaignBidding200Response get_campaign_bidding(campaign_id, account_id, platform, ad_account_id, customer_id)
Read a campaign's current bidding

Read of the campaign's bidding strategy on Google, cached for the quota window, for pre-filling the bid strategy block before a PUT to /v1/ads/campaigns/{campaignId}. Google Ads only; `platform` is required and rejected when it is anything else, since a `campaignId` is not globally unique. The response carries `cachedAt` and `stale`, set when a quota-exhausted call falls back to the last-good copy instead of a live read.  Maps Google's bidding strategy onto the same triplet PUT accepts: `LOWEST_COST_WITHOUT_CAP` (Maximize Conversions, no target), `COST_CAP` + `bidAmount` (Target CPA), `LOWEST_COST_WITH_MIN_ROAS` + `roasAverageFloor` (Target ROAS), `LOWEST_COST_WITH_BID_CAP` + `bidAmount` (Maximize Clicks with a CPC ceiling). A campaign on a portfolio strategy returns `portfolio` (id + name) and `bidSpec.portfolioBidStrategyId` instead of the triplet. Anything else (Manual CPC, Target Impression Share, ...) returns `bidSpec: null`; show `biddingStrategyType` as-is. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Numeric Google platform campaign id. | [required] |
**account_id** | **String** | Zernio Google Ads SocialAccount id: resolves the customer id + refresh token. | [required] |
**platform** | **String** | Required: campaign IDs are not globally unique. Only \"google\" is supported today. | [required] |
**ad_account_id** | Option<**String**> | Platform ad account ID (Google customer ID, digits only). Required when the connection has multiple Google Ads accounts; optional (and inferred) when it has only one. |  |
**customer_id** | Option<**String**> | Alias of adAccountId, kept for existing callers |  |

### Return type

[**models::GetCampaignBidding200Response**](getCampaignBidding_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_campaign_conversion_goals

> models::GetCampaignConversionGoals200Response get_campaign_conversion_goals(campaign_id)
Get campaign conversion goals

A Google campaign's conversion goals (CampaignConversionGoal, `biddable` per category and origin) and its goal config (ConversionGoalCampaignConfig): `goalConfigLevel` CUSTOMER means the campaign follows the account-default goals, CAMPAIGN means it uses its own goals or `customConversionGoalId`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Google campaign id | [required] |

### Return type

[**models::GetCampaignConversionGoals200Response**](getCampaignConversionGoals_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_campaign_targeting

> models::GetCampaignTargeting200Response get_campaign_targeting(campaign_id, platform)
Read a Google campaign's device, location, and language targeting

Google Ads compliance requires geo, language, budget, and bidding targeting set at creation to stay editable afterwards; this reads the campaign state so an integrator can build an editor around it. Cached for the quota window (10 minutes fresh, up to 7 days last-good), not always a live read. Google only; every other platform returns 501.  `devices` lists the device criteria the campaign carries, which depends on its channel: Search campaigns have MOBILE, DESKTOP and TABLET, Display campaigns also have CONNECTED_TV. `bidModifier` is Google's bid adjustment for that device, `null` when it has none, and `0` when the device is switched off; `included` is false for exactly that case. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Google platform campaign ID | [required] |
**platform** | Option<**String**> | Disambiguates when the same campaignId string exists on more than one connected platform. |  |

### Return type

[**models::GetCampaignTargeting200Response**](getCampaignTargeting_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_google_asset_group

> models::GetGoogleAssetGroup200Response get_google_asset_group(campaign_id, asset_group_id)
Get a Performance Max asset group

One asset group with its linked assets, ad strength, primary status and listing-group tree. Uses a 10-minute cache, served stale when Google quota is exhausted; any write below clears it.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Google Ads campaign id. | [required] |
**asset_group_id** | **String** | Google asset group id. | [required] |

### Return type

[**models::GetGoogleAssetGroup200Response**](getGoogleAssetGroup_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ad_campaigns

> models::ListAdCampaigns200Response list_ad_campaigns(include_empty, page, limit, source, platform, status, ad_account_id, campaign_id, page_id, account_id, profile_id, from_date, to_date, has_delivery, min_spend, live)
List campaigns

Returns campaigns as virtual aggregations over ad documents grouped by platform campaign ID. Metrics (spend, impressions, clicks, etc.) are summed across all ads in each campaign. Campaign status is derived from child ad statuses (active > pending_review > paused > error > completed > cancelled > rejected). Google campaign budgets include amountMicros, explicitlyShared, resourceName and deliveryMethod after the next successful sync. This endpoint does not fetch Google live.  **Status freshness.** `status`, `configuredStatus`, `platformStatus`, `platformAdSetStatus` and `platformCampaignStatus` are the values Zernio last stored. Background sync refreshes them, typically within 15 to 60 minutes (Google up to about 3 hours), and ended or long-paused objects may be refreshed less often. Zernio's own status writes re-read the switches they change. A change made in the platform's own ads manager therefore shows up here only after the next sync. Controllers that act on a switch should pass `live=true`, which reads the switches from the platform now, stores them, and returns `statusReadAt` (null when the read failed and the stored values were returned). With `live=true` (which needs `limit` of 20 or less) each returned campaign's own switch (`platformCampaignStatus`) is read live. Live reads cover TikTok, Meta, Google and OpenAI. The rolled-up `status` is not re-derived by a live read.  **Budgets here are SYNCED**, never read live, including with `live=true`. To read the current budgets (and status) of every campaign and ad set of a Meta ad account live in one call, for example as a pre-write spend gate, use GET /v1/ads/accounts/live. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**include_empty** | Option<**bool**> | Meta only. Campaign reads aggregate over ad documents, so a campaign with ZERO ads is normally invisible here, the state the two-step create (campaign, then ads via `existingCampaignId`) leaves behind whenever Meta rejects the ad step. Set true to list those too, with `adCount: 0` and zeroed metrics. Requires `accountId` and `adAccountId`, since an empty campaign has no ad row to resolve a token or ad account from. |  |
**page** | Option<**i32**> | Page number (1-based) |  |[default to 1]
**limit** | Option<**i32**> |  |  |[default to 20]
**source** | Option<**String**> | `all` (default) returns both Zernio-created ads and those discovered from the platform's ad manager. Matches the web UI's default view. Pass `zernio` to restrict to isExternal=false only. Status is NOT filtered by default; use the `status` param for that. |  |[default to all]
**platform** | Option<**String**> |  |  |
**status** | Option<[**AdStatus**](AdStatus.md)> | Filter by derived campaign status (post-aggregation) |  |
**ad_account_id** | Option<**String**> | Platform ad account ID (e.g. act_123 for Meta) |  |
**campaign_id** | Option<**String**> | Platform campaign ID (the `platformCampaignId` on each returned campaign). Returns only that campaign, or an empty list when it is not visible to the caller. Mirrors the same filter on /v1/ads and /v1/ads/tree. |  |
**page_id** | Option<**String**> | Meta only: Facebook Page ID. Campaigns have no Page of their own, so this keeps campaigns having at least one ad backed by this Page, with adCount and metrics computed over those ads only. Mirrors the same filter on /v1/ads and /v1/ads/tree. |  |
**account_id** | Option<**String**> | Account ID |  |
**profile_id** | Option<**String**> | Profile ID |  |
**from_date** | Option<**String**> | Start of metrics date range (YYYY-MM-DD, inclusive). Defaults to 90 days ago when both date params are omitted. |  |
**to_date** | Option<**String**> | End of metrics date range (YYYY-MM-DD, inclusive). Defaults to today. Max 730-day range. |  |
**has_delivery** | Option<**bool**> | Return only campaigns that delivered between `fromDate` and `toDate`: spend above zero, or impressions served at zero spend. Unlike `status`, which reads a campaign's CURRENT state, this filters on what happened inside the window. Filters the campaign set itself, so `pagination.total` counts only matching campaigns. Mirrors the same filter on /v1/ads/tree. |  |
**min_spend** | Option<**f64**> | Return only campaigns whose spend between `fromDate` and `toDate` reaches this amount, in each campaign's OWN currency (the `currency` field on the campaign). Implies `hasDelivery`; `minSpend=0` applies no filter. Mirrors the same filter on /v1/ads/tree. |  |
**live** | Option<**bool**> | Read the on/off switches live from the platform instead of returning the synced values. The fresh values are stored (so later reads return them too) and the response carries `statusReadAt`, the time of the read. At most 20 platform objects are read per request. Where a read fails (credentials, platform error, no reader on that platform), the stored values come back with `statusReadAt: null`. See \"Status freshness\" in the operation description. |  |[default to false]

### Return type

[**models::ListAdCampaigns200Response**](listAdCampaigns_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ad_group_assets

> models::ListAdGroupAssets200Response list_ad_group_assets(ad_set_id, account_id, ad_account_id, customer_id)
List ad-group assets

Lists directly attached Google assets. Fresh reads are cached for 10 minutes; exhausted quota may return the last successful read with stale=true. Inherited assets are not included.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_set_id** | **String** | Numeric Google platform id. | [required] |
**account_id** | **String** |  | [required] |
**ad_account_id** | Option<**String**> |  |  |
**customer_id** | Option<**String**> |  |  |

### Return type

[**models::ListAdGroupAssets200Response**](listAdGroupAssets_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ad_keywords

> models::ListAdKeywords200Response list_ad_keywords(page, limit, account_id, ad_account_id, profile_id, campaign_id, ad_set_id, status, match_type, negative, search)
List Search keywords

Returns the Google Search keyword criteria (positive and negative) synced from connected Google Ads accounts, one row per ad-group keyword. Refreshed about once a day per Google Ads customer (the keyword sweep rides the ads discovery pass on a slower slot), so keywords added on Google can take up to a day to appear. A customer synced for the first time is populated on the next discovery pass rather than waiting for its daily slot, and connecting an account or triggering a manual sync refreshes it immediately. Campaign-level negative keywords are not included; only ad-group-level criteria are. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**page** | Option<**i32**> | Page number (1-based) |  |[default to 1]
**limit** | Option<**i32**> |  |  |[default to 50]
**account_id** | Option<**String**> | Account ID |  |
**ad_account_id** | Option<**String**> | Platform ad account ID (Google customer ID). Mirrors the same filter on /v1/ads. |  |
**profile_id** | Option<**String**> | Profile ID |  |
**campaign_id** | Option<**String**> | Platform campaign ID |  |
**ad_set_id** | Option<**String**> | Platform ad group ID (Google ad group) |  |
**status** | Option<**String**> | Keyword criterion status |  |
**match_type** | Option<**String**> |  |  |
**negative** | Option<**bool**> | true = negative keywords only, false = positive only. Omit for both. |  |
**search** | Option<**String**> | Case-insensitive substring match on the keyword text |  |

### Return type

[**models::ListAdKeywords200Response**](listAdKeywords_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ad_sets

> models::ListAdSets200Response list_ad_sets(account_id, ad_account_id, campaign_id, ad_set_id, platform, live)
List ad sets

Ad sets (Google ad groups) synced for the connection, optionally filtered by platform and campaignId. Reads the `ad_sets` table directly, independent of the `ads` rollup GET /v1/ads/tree uses, so a newly created standalone ad group with no ad yet (POST /v1/ads/ad-sets, Google only) is visible here even though it is invisible in the tree until an ad joins it via `adSetId` on POST /v1/ads/create. Returns at most 500 rows, newest first.  **This list is SYNCED, not live** (refreshed by background sync, see below). Each row also carries the ad set's config (`targeting`, `bidStrategy`, `bidAmount`, `optimizationGoal`, `billingEvent`, `promotedObject`), so `?accountId=...&adAccountId=act_...` returns the config of every ad set of an ad account in one call, without a `campaignId`. To read budgets, status, targeting, promoted object and bid strategy of every campaign and ad set of a Meta ad account LIVE in one call (for example as a pre-write spend gate), use GET /v1/ads/accounts/live instead.  **Status freshness.** `status`, `configuredStatus`, `platformStatus`, `platformAdSetStatus` and `platformCampaignStatus` are the values Zernio last stored. Background sync refreshes them, typically within 15 to 60 minutes (Google up to about 3 hours), and ended or long-paused objects may be refreshed less often. Zernio's own status writes re-read the switches they change. A change made in the platform's own ads manager therefore shows up here only after the next sync. Controllers that act on a switch should pass `live=true`, which reads the switches from the platform now, stores them, and returns `statusReadAt` (null when the read failed and the stored values were returned). With `live=true` (which needs a `campaignId` or `adSetId` filter) each listed ad set's own switch (`platformAdSetStatus`) is read live, for the first 20 rows; later rows keep their synced value with `statusReadAt: null`. Live reads cover TikTok, Meta, Google and OpenAI. The rolled-up `status` is not re-derived by a live read. On TikTok the same live read also returns the ad group's applied `optimizationGoal` and `billingEvent`, as TikTok's adgroup/get reports them, so you can verify the goal TikTok applied rather than the one you requested. It also returns `nativeSettings`: TikTok's own adgroup/get record for the ad group, verbatim and read in that same call (budget, budget_mode, schedule, placements, locations, ages, gender, languages, interests, actions, audiences and exclusions), plus the advertiser's currency and timezone. TikTok's `schedule_start_time` / `schedule_end_time` are UTC wall clocks (\"YYYY-MM-DD HH:MM:SS\", no offset); Ads Manager displays them in `advertiser_timezone`. `configReadAt` says when it was read; it is null on every row whose native settings were not read now, so never treat a null as a match. These are read, not retained create payloads, and are not stored.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | Option<**String**> | Account ID |  |
**ad_account_id** | Option<**String**> | Platform ad account id (Meta act_<n>). Lists every synced ad set of that ad account; no campaignId needed. |  |
**campaign_id** | Option<**String**> | Platform campaign ID |  |
**ad_set_id** | Option<**String**> | Platform ad set ID |  |
**platform** | Option<**String**> |  |  |
**live** | Option<**bool**> | Read the on/off switches live from the platform instead of returning the synced values. The fresh values are stored (so later reads return them too) and the response carries `statusReadAt`, the time of the read. At most 20 platform objects are read per request. Where a read fails (credentials, platform error, no reader on that platform), the stored values come back with `statusReadAt: null`. See \"Status freshness\" in the operation description. |  |[default to false]

### Return type

[**models::ListAdSets200Response**](listAdSets_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ads

> models::AdsListResponse list_ads(page, limit, source, status, platform, account_id, ad_account_id, page_id, profile_id, campaign_id, ad_set_id, platform_ad_id, effective_object_story_id, effective_instagram_media_id, from_date, to_date)
List ads

Returns a paginated list of ads with metrics computed over an optional date range. Use source=all to include externally-synced ads from platform ad managers. If no date range is provided, defaults to the last 90 days. Date range is capped at 730 days max.  To find the Zernio ad behind a comment you see in Meta Business Manager, filter by platformAdId (the Meta ad ID), effectiveObjectStoryId (Facebook), or effectiveInstagramMediaId (Instagram). Those are the post/media the ad's engagement lives on, and are also returned on each ad's `creative` object. Then call GET /v1/ads/{adId}/comments with the returned ad id. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**page** | Option<**i32**> | Page number (1-based) |  |[default to 1]
**limit** | Option<**i32**> |  |  |[default to 50]
**source** | Option<**String**> | all (default) = Zernio-created + platform-discovered ads. zernio = restrict to Zernio-created only. |  |[default to all]
**status** | Option<[**AdStatus**](AdStatus.md)> |  |  |
**platform** | Option<**String**> |  |  |
**account_id** | Option<**String**> | Account ID |  |
**ad_account_id** | Option<**String**> | Platform ad account ID (e.g. act_123 for Meta). Mirrors the same filter on /v1/ads/campaigns and /v1/ads/tree. |  |
**page_id** | Option<**String**> | Meta only: Facebook Page ID. Returns only ads whose creative is backed by this Page (a Meta ad account serves ads for every Page in the Business Manager). Matches each ad's `creative.pageId`; ads with no page signal (rare IG-only creatives) never match. Mirrors the same filter on /v1/ads/campaigns and /v1/ads/tree. |  |
**profile_id** | Option<**String**> | Profile ID |  |
**campaign_id** | Option<**String**> | Platform campaign ID (filter ads within a campaign) |  |
**ad_set_id** | Option<**String**> | Platform ad set ID (filter ads within an ad set, the /{adset_id}/ads read of an adset-centric dashboard). |  |
**platform_ad_id** | Option<**String**> | Meta ad ID. Returns the ad with this platform-side ad ID. |  |
**effective_object_story_id** | Option<**String**> | Facebook `{pageId}_{postId}` of the post the ad's engagement lives on (Meta `effective_object_story_id`). Use to map a Business-Manager-visible post back to the Zernio ad. |  |
**effective_instagram_media_id** | Option<**String**> | Instagram media ID of the boosted post (Meta `effective_instagram_media_id`). Use to map a Business-Manager-visible IG post back to the Zernio ad. |  |
**from_date** | Option<**String**> | Start of metrics date range (YYYY-MM-DD). Defaults to 90 days ago. |  |
**to_date** | Option<**String**> | End of metrics date range (YYYY-MM-DD). Defaults to today. Max 730-day range. |  |

### Return type

[**models::AdsListResponse**](AdsListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_bid_strategies

> models::ListBidStrategies200Response list_bid_strategies(account_id, ad_account_id, customer_id, from_date, to_date)
List portfolio bid strategies

Bidding strategy report: type, status, campaign count, clicks, cost, cost per conversion, impressions, average CPC and conversions over the date range (default last 30 days). Reads Google's `bidding_strategy` resource, cached for the quota window. Draws on the shared Google Ads operations budget. The response carries `cachedAt` and `stale`, set when a quota-exhausted call falls back to the last-good copy instead of a live read.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Google ads SocialAccount id. | [required] |
**ad_account_id** | Option<**String**> | Platform ad account ID (Google customer ID, digits only). Defaults to the account's connected customer. |  |
**customer_id** | Option<**String**> | Alias of adAccountId, kept for existing callers |  |
**from_date** | Option<**String**> | Defaults to 30 days ago. |  |
**to_date** | Option<**String**> | Defaults to today. |  |

### Return type

[**models::ListBidStrategies200Response**](listBidStrategies_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_campaign_assets

> models::ListCampaignAssets200Response list_campaign_assets(campaign_id, account_id, ad_account_id, customer_id)
List campaign assets

Lists directly attached Google assets. Fresh reads are cached for 10 minutes; exhausted quota may return the last successful read with stale=true. Inherited assets are not included.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Numeric Google platform id. | [required] |
**account_id** | **String** |  | [required] |
**ad_account_id** | Option<**String**> |  |  |
**customer_id** | Option<**String**> |  |  |

### Return type

[**models::ListCampaignAssets200Response**](listCampaignAssets_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_campaign_negative_keyword_lists

> models::ListAdNegativeKeywordLists200Response list_campaign_negative_keyword_lists(campaign_id, platform)
List campaign negative lists

Returns shared negative keyword lists attached to the campaign, separate from campaign-level negative keywords. Google Ads shared negative keyword lists (shared_set type NEGATIVE_KEYWORDS). Reads are cached for 10 minutes; quota exhaustion may return the last successful result for up to 7 days with stale=true. Customer selection is limited to this connection and its account scope.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** |  | [required] |
**platform** | Option<**String**> |  |  |

### Return type

[**models::ListAdNegativeKeywordLists200Response**](listAdNegativeKeywordLists_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_campaign_negative_keywords

> models::ListCampaignNegativeKeywords200Response list_campaign_negative_keywords(campaign_id, platform)
List campaign-level negative keywords

Returns the campaign-level negative keywords (`campaign_criterion.negative`), distinct from the ad-group-level negatives under `GET /v1/ads/keywords`. Cached for the quota window (not synced to Postgres), and gated by the shared Google Ads operations budget like every other on-demand Google surface. The response carries `cachedAt` and `stale`, set when a quota-exhausted call falls back to the last-good copy instead of a live read.  The platform is always discovered from the campaign itself; a non-Google campaign returns 501 rather than 404, whether or not `platform` was passed. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Platform campaign ID | [required] |
**platform** | Option<**String**> | Optional and NOT authoritative: the resolved campaign's own platform decides 200 vs 501, never this hint. |  |

### Return type

[**models::ListCampaignNegativeKeywords200Response**](listCampaignNegativeKeywords_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_google_asset_groups

> models::ListGoogleAssetGroups200Response list_google_asset_groups(campaign_id)
List Performance Max asset groups

Read Performance Max asset groups and their linked text, image and YouTube assets. campaignId is the platform campaign id returned by creation or the campaign list. The campaign must be visible to the caller. Uses a 10-minute cache, with the last successful response served as stale when Google quota is exhausted. Removed groups and asset links are excluded. Campaign-level brand assets on campaigns with brand guidelines enabled are not included.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Google Ads campaign id. | [required] |

### Return type

[**models::ListGoogleAssetGroups200Response**](listGoogleAssetGroups_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_google_recommendations

> models::ListGoogleRecommendations200Response list_google_recommendations(account_id, ad_account_id, customer_id, campaign_id, types)
List Google Ads recommendations

Google's optimization recommendations for one ad account: type, estimated impact (base vs potential metrics, cost in account currency units), the campaign, ad group or budget they target, and the type-specific payload Google returns (`details`, in Google's own shape with micros). Filter by campaignId and types. Cached for 10 minutes and cleared by apply or dismiss; served stale when Google quota is exhausted.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Google ads SocialAccount id. | [required] |
**ad_account_id** | Option<**String**> | Google customer id, digits only. Defaults to the connection's only customer. |  |
**customer_id** | Option<**String**> | Alias of adAccountId, kept for consistency with other Google endpoints. |  |
**campaign_id** | Option<**String**> | Only recommendations targeting this campaign. |  |
**types** | Option<**String**> | Comma-separated Google RecommendationType values, for example CAMPAIGN_BUDGET,KEYWORD,SET_TARGET_CPA. |  |

### Return type

[**models::ListGoogleRecommendations200Response**](listGoogleRecommendations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_ad_group_assets

> models::RemoveCampaignAssets200Response remove_ad_group_assets(ad_set_id, remove_ad_group_assets_request)
Remove ad-group assets

Removes the specified attachments only. Google assets cannot be deleted. Other attachments remain. assetResourceNames is retained for compatibility.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_set_id** | **String** | Numeric Google platform id. | [required] |
**remove_ad_group_assets_request** | [**RemoveAdGroupAssetsRequest**](RemoveAdGroupAssetsRequest.md) |  | [required] |

### Return type

[**models::RemoveCampaignAssets200Response**](removeCampaignAssets_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_ad_keyword

> models::RemoveAdKeyword200Response remove_ad_keyword(keyword_id)
Remove a Search keyword

Removes one keyword criterion (positive or negative) from its ad group (M.140).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**keyword_id** | **String** | Zernio keyword ID (`id`), or Google's native `{adSetId}~{platformCriterionId}` (the tail of `resourceName`, e.g. 1234567890~987654321). A bare criterion id is rejected because it is only unique within its ad group. | [required] |

### Return type

[**models::RemoveAdKeyword200Response**](removeAdKeyword_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_campaign_assets

> models::RemoveCampaignAssets200Response remove_campaign_assets(campaign_id, remove_campaign_assets_request)
Remove campaign assets

Removes the specified attachments only. Google assets cannot be deleted. Other attachments remain. assetResourceNames is retained for compatibility.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Numeric Google platform id. | [required] |
**remove_campaign_assets_request** | [**RemoveCampaignAssetsRequest**](RemoveCampaignAssetsRequest.md) |  | [required] |

### Return type

[**models::RemoveCampaignAssets200Response**](removeCampaignAssets_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_google_asset_group

> models::RemoveGoogleAssetGroup200Response remove_google_asset_group(campaign_id, asset_group_id, validate_only)
Remove a Performance Max asset group

Removes the asset group on Google (status REMOVED, not reversible). Pass validateOnly=true to validate without removing.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** |  | [required] |
**asset_group_id** | **String** |  | [required] |
**validate_only** | Option<**bool**> |  |  |[default to false]

### Return type

[**models::RemoveGoogleAssetGroup200Response**](removeGoogleAssetGroup_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## replace_campaign_negative_keyword_lists

> models::ReplaceAdNegativeKeywordListKeywords200Response replace_campaign_negative_keyword_lists(campaign_id, replace_campaign_negative_keyword_lists_request)
Replace campaign negative lists

Sets the full desired set of shared negative keyword list associations on this campaign. Send listIds=[] to detach all negative keyword lists. Only campaign_shared_set links are changed; the lists and their keywords are preserved. Every list must belong to the campaign customer and have type NEGATIVE_KEYWORDS.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** |  | [required] |
**replace_campaign_negative_keyword_lists_request** | [**ReplaceCampaignNegativeKeywordListsRequest**](ReplaceCampaignNegativeKeywordListsRequest.md) |  | [required] |

### Return type

[**models::ReplaceAdNegativeKeywordListKeywords200Response**](replaceAdNegativeKeywordListKeywords_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## replace_campaign_negative_keywords

> models::ReplaceCampaignNegativeKeywords200Response replace_campaign_negative_keywords(campaign_id, replace_campaign_negative_keywords_request)
Replace campaign-level negative keywords

Replaces the FULL set of campaign-level negative keywords (C.270): the desired list is diffed against what Google already has, and the difference is applied as one `create`/`remove` mutate. Send an empty array to clear every campaign negative.  The platform is always discovered from the campaign itself; a non-Google campaign returns 501 rather than 404, whether or not `platform` was sent. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Platform campaign ID | [required] |
**replace_campaign_negative_keywords_request** | [**ReplaceCampaignNegativeKeywordsRequest**](ReplaceCampaignNegativeKeywordsRequest.md) |  | [required] |

### Return type

[**models::ReplaceCampaignNegativeKeywords200Response**](replaceCampaignNegativeKeywords_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## replace_google_listing_group_filters

> models::ReplaceGoogleListingGroupFilters200Response replace_google_listing_group_filters(campaign_id, asset_group_id, replace_google_listing_group_filters_request)
Replace an asset group's listing-group tree

Replace the product (listing-group) tree of a Performance Max retail asset group. The current tree is removed and the new one created in one atomic request. Read the current tree with GET on the asset group. Requires a campaign linked to Merchant Center; other campaigns return 400 LISTING_SOURCE_NOT_ALLOWED from Google. validateOnly: true validates without writing.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Google Ads campaign id. | [required] |
**asset_group_id** | **String** | Google asset group id. | [required] |
**replace_google_listing_group_filters_request** | [**ReplaceGoogleListingGroupFiltersRequest**](ReplaceGoogleListingGroupFiltersRequest.md) |  | [required] |

### Return type

[**models::ReplaceGoogleListingGroupFilters200Response**](replaceGoogleListingGroupFilters_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_ad

> models::UpdateAd200Response update_ad(ad_id, update_ad_request)
Update ad

Patch one or more fields on an ad. Status, budget, targeting, and creative changes are propagated to the platform.  Per-platform support: - **Meta** (Facebook + Instagram): all fields supported. - **TikTok**: status, budget, `name` (renames the ad), targeting (via `/v2/adgroup/update/`), and creative   (via `/v2/ad/update/` patch-style: `headline` is ignored, `body` becomes `ad_text`). - **Google**: status, budget, KEYWORD edits via `targeting.keywords` /   `targeting.negativeKeywords`, DEVICE bid adjustments via `targeting.devices`,   LOCATION edits via `targeting.locations` (or the equivalent top-level   `targeting.countries` / `regions` / `cities` / `zips` / `metros`), and LANGUAGE   edits via `targeting.languages`.   Each list you send becomes the FULL new set of its kind (criteria not in the   list are removed, except devices, which Google cannot remove and which are   switched off with a bid modifier of 0 instead); a kind left out is untouched.   Any other `targeting` field   returns 400: Google cannot mutate it post-create without recreating   the campaign. Creative edits are dispatched on the ad's `advertisingChannelType`,   and every supported field replaces a whole set; a field you omit is preserved.   - **Search**: top-level `headlines`, `descriptions` and `finalUrls`. Use 3-15 headlines     (1-30 characters) and 2-4 descriptions (1-90 characters). Omit an asset to remove it;     omit pinnedField on an included asset to unpin it. Updates do not pad or truncate text.     The legacy creative fields remain unsupported.   - **Display**: top-level `headlines` (1-5, no pinnedField, display ads have no pinned     positions), `descriptions` (1-5) and `finalUrls`, plus `creative.longHeadline`,     `creative.businessName`, `creative.imageUrl` (the landscape marketing image) and     `creative.squareImageUrl`. Each image URL is uploaded as a new Google asset and the ad     is pointed at it; Google assets are immutable, so the previous asset stays in the     account's asset library.   - **Performance Max**: top-level `assetGroup`, which swaps asset roles on the ad's asset     group. The other creative fields return 422 for this channel, and `assetGroup` returns     422 on any other channel.   - **Demand Gen**: top-level `demandGen` (see GoogleDemandGenUpdate): creative, channel     and audience changes in one atomic Google request. The other creative fields return     422 for this channel. `targeting` takes locations, languages, `locationTargetingType`     and `devices`; locations and languages are written to the ad's ad group, which     Demand Gen requires (campaigns migrated from Discovery that still target on the     campaign keep being written there), so they apply to every ad in that ad group. - **LinkedIn**: status, budget, targeting (countries or regions, excludedLocations (countries),   the B2B facets, and audience segments; applied to the LinkedIn Campaign via   PARTIAL_UPDATE, and REPLACES the campaign's entire targetingCriteria, not a merge),   and creative (uploads new media, creates a replacement inline creative on the same   campaign, pauses the old one). - **Pinterest / X / OpenAI Ads**: status + budget only. Sending   `targeting` or `creative` returns 501 with code `unsupported_platform_operation`.   OpenAI Ads budget is the campaign's spend cap, daily or lifetime (see `budget.type` below).  **Google location and language replacement:** locations, languages and devices are campaign-level criteria on Google, so these edits apply to every ad group and ad in the ad's campaign. Send the complete list you want to keep. Zernio diffs it against the campaign's live criteria and sends the removes and the creates in ONE `googleAds:mutate`, so the campaign is never left with a half-applied set; criteria already in the list keep their criterion ID and history. Excluded (negative) locations are left untouched. An empty location list returns 400 (a Google campaign with no location criteria targets every country, which is never what \"remove my locations\" means, so omit the field instead). Send either `targeting.locations` or the top-level geo fields, not both: mixing them returns 400.  **Google radius targeting:** `customLocations` is editable and is replaced the same way, but as its OWN set. Google models a place (LOCATION) and a point plus radius (PROXIMITY) as different criterion types, so the two are independent: sending `customLocations` replaces every radius and leaves the cities and countries alone, and sending places replaces those and leaves the radius alone. Send `customLocations: []` to drop radius targeting entirely. A circle you re-send unchanged keeps its criterion ID rather than being removed and recreated.  **Google keyword replacement:** These edits affect the ad's entire ad group, including sibling ads. Positive (`targeting.keywords`) and negative (`targeting.negativeKeywords`) sets are independent: omit a field to leave that set unchanged, or send `[]` to remove every keyword of that kind.  Zernio compares each supplied set with Google's live criteria by case-insensitive keyword text and match type. A matching criterion is left untouched, retaining its criterion ID, enabled/paused status, keyword-level bid overrides, labels, and criterion-associated history/statistics. Zernio does not reset its quality score; Google continues to calculate scores and statistics normally. Text comparison does not trim whitespace.  A bare string or an object without `matchType` means `broad`, not the existing criterion's match type. For example, resending an existing `{ \"text\": \"plumber\", \"matchType\": \"exact\" }` preserves it; sending `\"plumber\"` instead removes that EXACT criterion and requests a BROAD one. Changing text or match type removes criteria no longer requested and creates any missing criteria. New criteria get new IDs and do not inherit removed criteria's bid overrides, labels, or history. Historical reporting for a removed criterion is not transferred to its replacement.  To add keywords without replacing a set, use [POST /v1/ads/keywords](https://docs.zernio.com/ad-campaigns/add-ad-keywords). Use `PATCH /v1/ads/keywords/{keywordId}` to pause/enable one keyword, or `DELETE /v1/ads/keywords/{keywordId}` to remove it. 

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


## update_ad_campaign

> models::UpdateAdCampaign200Response update_ad_campaign(campaign_id, update_ad_campaign_request)
Update a campaign

Campaign-level edits. Send at least one of `budget`, `bidStrategy`, `portfolioBidStrategyId`, `name` or `platformSpecificData`. An unsupported field is always an error, never a silent drop.  | Body field | Meta | Google | Others | |---|---|---|---| | `bidStrategy` | Yes | Yes | 501 | | `bidAmount`, `roasAverageFloor` | 400 (ad-set level) | Yes | 400 | | `portfolioBidStrategyId` | 400 | Yes | 400 | | `budget` (CBO; ABO returns 409) | Yes | Daily only | OpenAI: daily or lifetime; others 501 | | `name` | Yes | 501 | 501 | | `platformSpecificData.spendCap` | Yes | 400 | 400 | | `accountId` (empty campaigns) | Yes | - | - |  Meta budget edits check the live campaign budget, so an older local ABO stamp cannot block a CBO campaign. A successful edit repairs local ad budget fields. A live ABO campaign still returns 409 with the ad-set budget endpoint.  On Google: `LOWEST_COST_WITHOUT_CAP` = Maximize Conversions, `COST_CAP` + `bidAmount` = Target CPA, `LOWEST_COST_WITH_MIN_ROAS` + `roasAverageFloor` = Target ROAS, `LOWEST_COST_WITH_BID_CAP` + `bidAmount` = Maximize Clicks with a CPC ceiling; `portfolioBidStrategyId` attaches a portfolio strategy instead (exclusive with `bidStrategy`). Setting the standard triplet on a campaign that is currently on a PORTFOLIO strategy is rejected: detach it in Google Ads first, since it is shared across campaigns.  Google budget updates read the current budget before mutation. Shared budgets return 409 unless allowSharedBudgetUpdate=true is explicitly supplied, because the change affects every campaign using that budget. Unknown sharing state also returns 409.  OpenAI Ads campaigns carry exactly one spend cap: `budget.type` daily or lifetime replaces whichever cap the campaign had, with a minimum of 1 in the ad account's currency (422 below it). Lifetime can switch to daily, but OpenAI never switches a daily cap back to lifetime (422).  `accountId` forwards the update straight to Meta for a campaign with zero ads, which would otherwise 404; the response then carries `updated: 0`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Platform campaign ID | [required] |
**update_ad_campaign_request** | [**UpdateAdCampaignRequest**](UpdateAdCampaignRequest.md) |  | [required] |

### Return type

[**models::UpdateAdCampaign200Response**](updateAdCampaign_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_ad_campaign_status

> models::UpdateAdCampaignStatus200Response update_ad_campaign_status(campaign_id, update_ad_campaign_status_request)
Pause or resume a campaign

Writes the campaign's own on/off switch and nothing else, on every platform (Meta, TikTok, Google, LinkedIn campaign group, Pinterest, X, ChatGPT (OpenAI)). Its ad sets and ads keep their own switches: pausing stops their delivery through the campaign, and resuming lets each of them deliver again only if its own switch is on. An ad set or ad you paused individually stays paused; resume it with PUT /v1/ads/ad-sets/{adSetId}/status or PUT /v1/ads/{adId}/status. See the Status model in the Ad Campaigns tag.  **Live read, then write.** The campaign's switch is read from the platform first. When that live read shows it already in the requested state nothing is written (`updated: 0`, `skipped: 1`, with the reason). Otherwise the switch is written (`updated: 1`), read back and stored, and the delivery status of the ads under it (up to 20) is re-read and stored, so an immediate GET returns what the platform now reports. A stored switch never skips a write, and when the platform cannot be read the write always goes out. On Meta the check reads the campaign's own `status`, so a delivery status such as `IN_PROCESS` or `WITH_ISSUES` does not force a write. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Platform campaign ID | [required] |
**update_ad_campaign_status_request** | [**UpdateAdCampaignStatusRequest**](UpdateAdCampaignStatusRequest.md) |  | [required] |

### Return type

[**models::UpdateAdCampaignStatus200Response**](updateAdCampaignStatus_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_ad_group_assets

> models::UpdateCampaignAssets200Response update_ad_group_assets(ad_set_id, update_campaign_assets_request)
Update ad-group assets

Edits existing Google assets in place. Send updates with assetResourceName and the fields to change. An asset is shared: changes affect every attachment using it. Omitted fields stay unchanged. The operation consumes the Google operations budget and invalidates affected cached lists.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_set_id** | **String** | Numeric Google platform id. | [required] |
**update_campaign_assets_request** | [**UpdateCampaignAssetsRequest**](UpdateCampaignAssetsRequest.md) |  | [required] |

### Return type

[**models::UpdateCampaignAssets200Response**](updateCampaignAssets_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_ad_keyword

> models::UpdateAdKeyword200Response update_ad_keyword(keyword_id, update_ad_keyword_request)
Pause or enable a Search keyword

Changes `ad_group_criterion.status` for one keyword criterion (M.140). Negative keywords have no status on Google and cannot be paused or enabled. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**keyword_id** | **String** | Zernio keyword ID (`id`), or Google's native `{adSetId}~{platformCriterionId}` (the tail of `resourceName`, e.g. 1234567890~987654321). A bare criterion id is rejected because it is only unique within its ad group. | [required] |
**update_ad_keyword_request** | [**UpdateAdKeywordRequest**](UpdateAdKeywordRequest.md) |  | [required] |

### Return type

[**models::UpdateAdKeyword200Response**](updateAdKeyword_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_ad_set

> models::UpdateAdSet200Response update_ad_set(ad_set_id, update_ad_set_request)
Update an ad set

Ad-set-level writes. Use this for ABO budget updates, ad-set-scoped pause/resume, bid-strategy edits, Meta value-rule-set attach/detach, and Meta-only post-launch delivery settings via `platformSpecificData`. At least one updatable field is required.  Value rule sets (Meta only, see `/v1/ads/value-rule-sets`): - ATTACH or REPLACE: send `valueRuleSetId`. Attachment is driven by the id's   presence, so `valueRulesApplied: true` is optional. Sending a different id   replaces the previous association; there is no separate replace call. - DETACH: send `valueRulesApplied: false` and OMIT `valueRuleSetId`. - Sending `valueRulesApplied: false` TOGETHER with `valueRuleSetId` returns 400   `mutually_exclusive_fields`. This is deliberate: Meta attaches the rule set   whenever `value_rule_set_id` is present, even with `value_rules_applied` false,   so echoing stored state while asking to detach would silently keep the bid   adjustments live. - Eligibility: only ad sets on `LOWEST_COST_WITHOUT_CAP` or `COST_CAP`. Meta   rejects the rest server-side. - Read back with `GET /v1/ads/ad-sets/{adSetId}?fields=value_rule_set_id`. Meta   does not document `value_rules_applied` as a readable ad-set field, so the   boolean cannot be read back.  Bid strategy compatibility (per Meta's spec): - `LOWEST_COST_WITHOUT_CAP`: no `bidAmount`, no `roasAverageFloor`. - `LOWEST_COST_WITH_BID_CAP` / `COST_CAP`: `bidAmount` REQUIRED (whole currency units). - `LOWEST_COST_WITH_MIN_ROAS`: `roasAverageFloor` REQUIRED (decimal multiplier, e.g. 2.0 = 2.0x ROAS). - Meta only: send `bidAmount` WITHOUT `bidStrategy` to change the cap amount on an ad set   under a COST_CAP / LOWEST_COST_WITH_BID_CAP parent campaign, leaving the strategy itself   (inherited from the campaign) untouched. `roasAverageFloor` without `bidStrategy` is   rejected (it has no meaning outside LOWEST_COST_WITH_MIN_ROAS).  Delivery settings are validated by Meta against the campaign objective; incompatible combinations (e.g. a billingEvent the optimization goal doesn't allow) surface as 400s from Meta.  When updating `budget` on an ABO campaign: if the parent campaign is CBO, the response is 409 with code BUDGET_LEVEL_MISMATCH. Route to PUT /v1/ads/campaigns/{campaignId} instead.  `status` behaves exactly as PUT /v1/ads/ad-sets/{adSetId}/status describes: only the ad set's own switch is written, its ads keep theirs, and `statusUpdated` / `statusSkipped` report whether that switch was written or a live read showed it already in place. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_set_id** | **String** | Platform ad set ID | [required] |
**update_ad_set_request** | [**UpdateAdSetRequest**](UpdateAdSetRequest.md) |  | [required] |

### Return type

[**models::UpdateAdSet200Response**](updateAdSet_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_ad_set_status

> models::UpdateAdSetStatus200Response update_ad_set_status(ad_set_id, update_ad_campaign_status_request)
Pause or resume a single ad set

Ad-set-scoped pause/resume (doesn't touch sibling ad sets). Thin wrapper over PUT /v1/ads/ad-sets/{adSetId} for callers that only want the status toggle and prefer a symmetric URL to /v1/ads/campaigns/{campaignId}/status.  Writes the ad set's own on/off switch and nothing else, on every platform (Meta `configured_status`, TikTok ad group `operation_status`, Google ad group status, LinkedIn campaign, Pinterest ad group, X line item, ChatGPT (OpenAI) ad group). Its ads keep their own switches: an ad you paused individually stays paused when the ad set resumes. The campaign above is not touched either, so an ad set resumed under a paused campaign reads `status: paused` until the campaign is resumed too. See the Status model in the Ad Campaigns tag.  **Live read, then write.** The ad set's switch is read from the platform first. When that live read shows it already in the requested state nothing is written (`updated: 0`, `skipped: 1`, with the reason). Otherwise the switch is written (`updated: 1`), read back and stored, and the delivery status of its ads (up to 20) is re-read and stored, so an immediate GET returns what the platform now reports. A stored switch never skips a write, and when the platform cannot be read the write always goes out. On Meta the check reads the ad set's own `status`, so a repeated request skips even while `platformAdSetStatus` reads `CAMPAIGN_PAUSED`, `WITH_ISSUES` or `IN_PROCESS`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_set_id** | **String** | Platform ad set ID | [required] |
**update_ad_campaign_status_request** | [**UpdateAdCampaignStatusRequest**](UpdateAdCampaignStatusRequest.md) |  | [required] |

### Return type

[**models::UpdateAdSetStatus200Response**](updateAdSetStatus_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_ad_status

> models::UpdateAdStatus200Response update_ad_status(ad_id, update_ad_keyword_request)
Pause or resume a single ad

Ad-scoped pause/resume: flips ONLY this ad's own switch (Meta `configured_status`, TikTok `operation_status`, Google ad group ad status, LinkedIn creative, Pinterest ad), never its parent ad set or campaign, so sibling ads keep running. X is the exception: its smallest switch is the line item. Thin wrapper over the `status` field of PUT /v1/ads/{adId}, for callers that want a URL symmetric to /v1/ads/campaigns/{campaignId}/status and /v1/ads/ad-sets/{adSetId}/status.  The ad's own switch is independent of its delivery status. An ad paused only because its campaign or ad set is off (`status: paused`, `configuredStatus: ACTIVE`) can still be switched off here, and switching an ad on under a paused campaign leaves it `paused` until the campaign is resumed. After the write the switch is read back from the platform and returned as `configuredStatus`, together with the resulting delivery `status`.  `{adId}` accepts the same identifier dialects as GET/PUT /v1/ads/{adId} (Zernio hex `_id`, Meta numeric `platformAdId`, or the creative's effective story/media IDs). `platform` is inferred from the ad, so it's not required in the body. Ads in terminal statuses (rejected, completed, cancelled) are skipped, and so is a request whose target already matches the ad's own switch as read LIVE from the platform (a stored value is never trusted alone, since the switch may have been changed in the platform's own UI). A skip also returns that live read. The rolled-up `status` never decides a skip. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_id** | **String** | Zernio `_id` (hex), Meta `platformAdId` (numeric), or one of the creative's effective story/media IDs. | [required] |
**update_ad_keyword_request** | [**UpdateAdKeywordRequest**](UpdateAdKeywordRequest.md) |  | [required] |

### Return type

[**models::UpdateAdStatus200Response**](updateAdStatus_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_bid_strategy

> models::UpdateBidStrategy200Response update_bid_strategy(strategy_id, update_bid_strategy_request)
Update portfolio bid strategy

Renames or retargets a portfolio bid strategy. The strategy's status is output only on Google's side, so it cannot be changed here; remove a strategy in Google Ads. `type` is only needed alongside `targetCpa`/`targetRoas` to disambiguate the field Google writes to (TARGET_CPA and MAXIMIZE_CONVERSIONS both take a target CPA; TARGET_ROAS and MAXIMIZE_CONVERSION_VALUE both take a target ROAS); the strategy's family is otherwise immutable once created.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**strategy_id** | **String** | Numeric Google Ads bid strategy id. | [required] |
**update_bid_strategy_request** | [**UpdateBidStrategyRequest**](UpdateBidStrategyRequest.md) |  | [required] |

### Return type

[**models::UpdateBidStrategy200Response**](updateBidStrategy_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_campaign_ad_schedule

> models::UpdateCampaignAdSchedule200Response update_campaign_ad_schedule(campaign_id, update_campaign_ad_schedule_request)
Replace a campaign's ad schedule (dayparting)

Replaces the campaign's whole ad schedule with the windows you send. This is a REPLACE, not a merge: windows you leave out stop serving.  Send `schedule: []` to clear dayparting, which returns the campaign to serving around the clock.  Google rules enforced here, so you get a named field instead of a criterion error: at most 6 windows per day, a window must end after it starts, windows on the same day may not overlap, `endHour` 24 is midnight and cannot carry minutes, and minutes are quarter-hours only (0, 15, 30, 45). `bidModifier` is 0.1-10.0; Google's 0 means \"off\" for devices only, so a window is switched off by leaving it out.  Windows are half-open (Google is exclusive of the end minute), so 09:00-12:00 and 12:00-17:00 on the same day are adjacent and both valid.  Google cannot edit an ad schedule in place (every AdScheduleInfo field is prohibited on update), so this removes the live criteria and creates the new ones in a single atomic mutate. The response is read back from Google and carries the new criterion ids. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Numeric Google platform campaign id. | [required] |
**update_campaign_ad_schedule_request** | [**UpdateCampaignAdScheduleRequest**](UpdateCampaignAdScheduleRequest.md) |  | [required] |

### Return type

[**models::UpdateCampaignAdSchedule200Response**](updateCampaignAdSchedule_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_campaign_assets

> models::UpdateCampaignAssets200Response update_campaign_assets(campaign_id, update_campaign_assets_request)
Update campaign assets

Edits existing Google assets in place. Send updates with assetResourceName and the fields to change. An asset is shared: changes affect every attachment using it. Omitted fields stay unchanged. The operation consumes the Google operations budget and invalidates affected cached lists.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Numeric Google platform id. | [required] |
**update_campaign_assets_request** | [**UpdateCampaignAssetsRequest**](UpdateCampaignAssetsRequest.md) |  | [required] |

### Return type

[**models::UpdateCampaignAssets200Response**](updateCampaignAssets_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_campaign_conversion_goals

> models::UpdateCampaignConversionGoals200Response update_campaign_conversion_goals(campaign_id, update_campaign_conversion_goals_request)
Update campaign conversion goals

Sets `biddable` on campaign goals, switches `goalConfigLevel`, and/or points the campaign at a custom conversion goal, in one mutate. `customConversionGoalId: null` clears it; Google refuses that (400) while the campaign stays at CAMPAIGN level with no biddable goals, so send `goalConfigLevel: CUSTOMER` with it to fall back to the account goals. Returns the re-read campaign goals.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Google campaign id | [required] |
**update_campaign_conversion_goals_request** | [**UpdateCampaignConversionGoalsRequest**](UpdateCampaignConversionGoalsRequest.md) |  | [required] |

### Return type

[**models::UpdateCampaignConversionGoals200Response**](updateCampaignConversionGoals_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_campaign_targeting

> models::UpdateCampaignTargeting200Response update_campaign_targeting(campaign_id, update_campaign_targeting_request)
Edit a Google campaign's device, location, or language targeting

Google Ads compliance row M.10: geo and language targeting set at creation must stay editable afterwards. Send at least one of `devices`, `locations`, `languages`, `locationTargetingType`; each provided field REPLACES that field's existing criteria on the campaign (a full set, not a delta). Fields left out of the body are untouched. Google only; every other platform returns 501.  `devices` is the full set of device bid modifiers: a supported device you leave out is switched off with a bid modifier of 0, since Google cannot remove a device criterion. A device the campaign's channel does not carry, and a set that switches every device off, both return 422.  `locations` accepts the same shapes as campaign creation: a bare array of ISO country codes, or an object with `countries`/`regions`/`cities`/`zips`/`metros` key lists (`key` from GET /v1/ads/targeting/search?dimension=geo). Negative (excluded) locations are left untouched by this endpoint. An empty location list returns 400 instead of removing every criterion: a Google campaign with no location criteria targets every country, so omit `locations` to leave targeting alone.  The removes and the creates go out in ONE Google `googleAds:mutate`, so a failed edit leaves the campaign's previous set intact rather than a half-applied one.  `languages` is an array of Google's language codes (ISO 639-1, plus variants such as `zh_CN`); an unknown code returns 400.  `locationTargetingType` switches who the location targeting reaches: `presence` (people in or regularly in the locations) or `presence_or_interest` (also people searching for or interested in them). Example: `{ \"platform\": \"google\", \"targeting\": { \"locationTargetingType\": \"presence\" } }`.  The response includes the refreshed `devices`/`locations`/`languages` state read back from Google after the edit, and invalidates the cached copy `GET` on this campaign would otherwise keep serving.  **Demand Gen:** Google keeps a Demand Gen campaign's locations and languages on its ad groups and refuses them on the campaign. When the campaign has one ad group they are written there and the response carries its `adGroupId` (the campaign-level `locations`/`languages` read back then stay empty). With several ad groups the call returns 400 naming them: edit each one with PUT /v1/ads/{adId} `targeting` on an ad of that ad group. Campaigns migrated from Discovery that still target on the campaign keep being written there. `devices` and `locationTargetingType` stay campaign-level. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Google platform campaign ID | [required] |
**update_campaign_targeting_request** | [**UpdateCampaignTargetingRequest**](UpdateCampaignTargetingRequest.md) |  | [required] |

### Return type

[**models::UpdateCampaignTargeting200Response**](updateCampaignTargeting_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_google_asset_group

> models::UpdateGoogleAssetGroup200Response update_google_asset_group(campaign_id, asset_group_id, update_google_asset_group_request)
Update a Performance Max asset group

Change the name, status (ENABLED or PAUSED), final URLs or display paths. Only the fields sent are written; null on path1 or path2 clears it. Change assets with the /assets endpoint and product targeting with /listing-group-filters. validateOnly: true validates without writing.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Google Ads campaign id. | [required] |
**asset_group_id** | **String** | Google asset group id. | [required] |
**update_google_asset_group_request** | [**UpdateGoogleAssetGroupRequest**](UpdateGoogleAssetGroupRequest.md) |  | [required] |

### Return type

[**models::UpdateGoogleAssetGroup200Response**](updateGoogleAssetGroup_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

