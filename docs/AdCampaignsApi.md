# \AdCampaignsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**boost_post**](AdCampaignsApi.md#boost_post) | **POST** /v1/ads/boost | Boost post as ad
[**bulk_update_ad_campaign_status**](AdCampaignsApi.md#bulk_update_ad_campaign_status) | **POST** /v1/ads/campaigns/bulk-status | Pause or resume many campaigns
[**create_ad_campaign**](AdCampaignsApi.md#create_ad_campaign) | **POST** /v1/ads/campaigns | Create a standalone campaign
[**create_standalone_ad**](AdCampaignsApi.md#create_standalone_ad) | **POST** /v1/ads/create | Create standalone ad
[**delete_ad**](AdCampaignsApi.md#delete_ad) | **DELETE** /v1/ads/{adId} | Cancel an ad
[**delete_ad_campaign**](AdCampaignsApi.md#delete_ad_campaign) | **DELETE** /v1/ads/campaigns/{campaignId} | Delete a campaign
[**duplicate_ad**](AdCampaignsApi.md#duplicate_ad) | **POST** /v1/ads/{adId}/duplicate | Duplicate an ad
[**duplicate_ad_campaign**](AdCampaignsApi.md#duplicate_ad_campaign) | **POST** /v1/ads/campaigns/{campaignId}/duplicate | Duplicate a campaign
[**duplicate_ad_set**](AdCampaignsApi.md#duplicate_ad_set) | **POST** /v1/ads/ad-sets/{adSetId}/duplicate | Duplicate an ad set
[**get_ad**](AdCampaignsApi.md#get_ad) | **GET** /v1/ads/{adId} | Get ad details
[**get_ad_set_details**](AdCampaignsApi.md#get_ad_set_details) | **GET** /v1/ads/ad-sets/{adSetId} | Live ad-set details incl. learning phase
[**get_ad_tree**](AdCampaignsApi.md#get_ad_tree) | **GET** /v1/ads/tree | Get campaign tree
[**get_ads_timeline**](AdCampaignsApi.md#get_ads_timeline) | **GET** /v1/ads/timeline | Get daily account metrics
[**list_ad_campaigns**](AdCampaignsApi.md#list_ad_campaigns) | **GET** /v1/ads/campaigns | List campaigns
[**list_ads**](AdCampaignsApi.md#list_ads) | **GET** /v1/ads | List ads
[**update_ad**](AdCampaignsApi.md#update_ad) | **PUT** /v1/ads/{adId} | Update ad
[**update_ad_campaign**](AdCampaignsApi.md#update_ad_campaign) | **PUT** /v1/ads/campaigns/{campaignId} | Update a campaign
[**update_ad_campaign_status**](AdCampaignsApi.md#update_ad_campaign_status) | **PUT** /v1/ads/campaigns/{campaignId}/status | Pause or resume a campaign
[**update_ad_set**](AdCampaignsApi.md#update_ad_set) | **PUT** /v1/ads/ad-sets/{adSetId} | Update an ad set
[**update_ad_set_status**](AdCampaignsApi.md#update_ad_set_status) | **PUT** /v1/ads/ad-sets/{adSetId}/status | Pause or resume a single ad set
[**update_ad_status**](AdCampaignsApi.md#update_ad_status) | **PUT** /v1/ads/{adId}/status | Pause or resume a single ad



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


## bulk_update_ad_campaign_status

> models::BulkUpdateAdCampaignStatus200Response bulk_update_ad_campaign_status(bulk_update_ad_campaign_status_request)
Pause or resume many campaigns

Process up to 50 campaigns in one call. Each campaign is updated concurrently and the response contains a per-campaign result so a single bad row does not fail the whole batch. 

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

> models::CreateAdCampaign201Response create_ad_campaign(create_ad_campaign_request)
Create a standalone campaign

Creates a campaign WITHOUT its first ad set / ad (the ODAX shell only). Ad sets join it later via `existingCampaignId` on the create endpoints. A budget here is campaign-level (CBO) by definition; omit it for ABO (each ad set carries its own budget). Created `PAUSED` unless `status: ACTIVE`. The campaign materializes in `/v1/ads/tree` via the next sync discovery pass.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_ad_campaign_request** | [**CreateAdCampaignRequest**](CreateAdCampaignRequest.md) |  | [required] |

### Return type

[**models::CreateAdCampaign201Response**](createAdCampaign_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_standalone_ad

> models::CreateStandaloneAd200Response create_standalone_ad(create_standalone_ad_request, idempotency_key)
Create standalone ad

Creates a paid ad with custom creative across Meta, Google Ads, Pinterest, TikTok, X/Twitter, and LinkedIn. Supports three mutually-exclusive request shapes selected by the body, a legacy single-creative shape (all platforms, default), a Meta-only multi-creative shape via the creatives array (one ad set with N ads sharing budget and targeting), and a Meta-only attach shape via adSetId (adds one new ad to an existing ad set). Per-platform required fields, budget minimums, and video-ad rules are documented on each property below. LinkedIn creates a Single Image or Single Video Ad backed by a Direct Sponsored Content \"dark post\" authored by a Company Page (see `organizationId`); supported goals are engagement, traffic, awareness, and video_views (video ads use the `video` field; video_views requires a video), and traffic ads require `linkUrl`.  **Idempotency:** this endpoint is not idempotent at the platform level (a blind retry creates a second campaign/ad set/ad). Send an `Idempotency-Key` header to make retries safe: the first request with a given key creates the ad and we store the response; a retry with the same key replays that exact response (with `Idempotent-Replayed: true`) instead of creating duplicates. Reusing a key with a different body returns 422; a key whose first request is still in flight returns 409 (retry after a short backoff). Keys are scoped to your credential and expire after 24h.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_standalone_ad_request** | [**CreateStandaloneAdRequest**](CreateStandaloneAdRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes create retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. |  |

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


## delete_ad_campaign

> models::DeleteAdCampaign200Response delete_ad_campaign(campaign_id, delete_ad_campaign_request)
Delete a campaign

Deletes the whole campaign on the platform, cascading to its ad sets and ads. Locally, all Ad documents for this campaign are marked `status: cancelled`.  Meta-only for now. Other platforms return 501 Not Implemented — fall back to DELETE /v1/ads/{adId} per ad in the meantime. 

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


## duplicate_ad

> models::DuplicateAd200Response duplicate_ad(ad_id, duplicate_ad_request)
Duplicate an ad

Duplicates a single ad via Meta's native `POST /{ad-id}/copies`. The copy is created paused. `adSetId` retargets the copy into another ad set; omitted = the source's own ad set. Accepts the Zernio ad id or the platform ad id. Sync discovery is triggered automatically (`syncAfter: false` to skip).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_id** | **String** | Zernio ad ID or platform ad ID | [required] |
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

> models::DuplicateAdCampaign200Response duplicate_ad_campaign(campaign_id, duplicate_ad_campaign_request)
Duplicate a campaign

Duplicates a campaign, including its ad sets, ads, creatives, and targeting by default (`deepCopy: true`). The copy is created paused so callers can review before launching.  Per-platform implementation: - **Meta** uses the native `POST /{campaign-id}/copies` endpoint. - **TikTok** has no native copy primitive; Zernio walks the source   graph (`/v2/campaign/get/`, `/v2/adgroup/get/`, `/v2/ad/get/`) and   recreates each entity via the corresponding `/create/` endpoints,   carrying over budget / targeting / bid_type / bid_price /   deep_bid_type / creative fields. Spark Ad linkage (`tiktok_item_id`)   is preserved. - **LinkedIn** has no native copy primitive; Zernio walks the source   CampaignGroup → Campaigns → Creatives and recreates each entity,   carrying over `type` / `costType` / `unitCost` /   `optimizationTargetType` / `creativeSelection` / `objectiveType` /   `format` / `dailyBudget` / `totalBudget` / `targetingCriteria` /   `runSchedule` and every Creative's `content` object verbatim.   `statusOption: INHERITED_FROM_SOURCE` is evaluated **per entity**:   any Group / Campaign / Creative whose source is `ACTIVE` gets its   clone activated too. Duplicating an ACTIVE campaign with   `INHERITED_FROM_SOURCE` starts a second front of spend the moment   the clone activates — the safe default is `PAUSED`.  The new hierarchy is asynchronous to materialize in our DB — we trigger sync discovery automatically. Set `syncAfter: false` to skip and poll `/v1/ads/tree` on your own cadence.  Other platforms return 501 Not Implemented. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Source platform campaign ID | [required] |
**duplicate_ad_campaign_request** | [**DuplicateAdCampaignRequest**](DuplicateAdCampaignRequest.md) |  | [required] |

### Return type

[**models::DuplicateAdCampaign200Response**](duplicateAdCampaign_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## duplicate_ad_set

> models::DuplicateAdSet200Response duplicate_ad_set(ad_set_id, duplicate_ad_set_request)
Duplicate an ad set

Duplicates an ad set, including its ads and creatives by default (`deepCopy: true`), via Meta's native `POST /{adset-id}/copies`. The copy is created paused so callers can review before launching. `campaignId` retargets the copy into another campaign; omitted = the source's own campaign. The new hierarchy materializes asynchronously — sync discovery is triggered automatically (`syncAfter: false` to skip).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_set_id** | **String** | Source platform ad set ID | [required] |
**duplicate_ad_set_request** | [**DuplicateAdSetRequest**](DuplicateAdSetRequest.md) |  | [required] |

### Return type

[**models::DuplicateAdSet200Response**](duplicateAdSet_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad

> models::GetAd200Response get_ad(ad_id)
Get ad details

Returns an ad with its creative, targeting, status, and performance metrics.  The `{adId}` path segment accepts any identifier dialect Zernio indexes for the ad: - the Zernio internal `_id` (24-char hex) - Meta's numeric `platformAdId` (the value shipped in `comment.received` webhooks as `comment.ad.id`) - the creative's `effective_object_story_id` (`{pageId}_{postId}` shape, Facebook side) - the creative's `effective_instagram_media_id` (Instagram side)  Any of the four resolve to the same ad. Caller doesn't need a translation step. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_id** | **String** | Zernio `_id` (hex), Meta `platformAdId` (numeric), or one of the creative's effective story/media IDs. See description for details.  | [required] |

### Return type

[**models::GetAd200Response**](getAd_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad_set_details

> models::GetAdSetDetails200Response get_ad_set_details(ad_set_id, account_id, fields)
Live ad-set details incl. learning phase

Reads the ad set live from Meta, returned verbatim. The default projection includes `learning_stage_info` (learning-phase status: LEARNING / SUCCESS / FAIL / WAIVING — Meta omits its `status` key on paused ad sets), delivery settings, budgets, schedule and targeting. `fields` is a raw-passthrough override; unknown fields return Meta's 400 verbatim.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_set_id** | **String** | Meta ad set id (platformAdSetId). | [required] |
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. | [required] |
**fields** | Option<**String**> | Comma-separated Graph field override (supports nested {} projections). |  |

### Return type

[**models::GetAdSetDetails200Response**](getAdSetDetails_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad_tree

> models::GetAdTree200Response get_ad_tree(page, limit, source, platform, status, ad_account_id, account_id, profile_id, campaign_id, from_date, to_date, sort, time_increment, daily_level)
Get campaign tree

Returns a nested Campaign > Ad Set > Ad hierarchy with rolled-up metrics at each level. Uses a two-stage aggregation: ads are grouped into ad sets, then ad sets into campaigns. Metrics are computed over an optional date range, then rolled up from ad level to ad set and campaign levels. Pagination is at the campaign level. Ads without a campaign or ad set ID are grouped into synthetic \"Ungrouped\" buckets. If no date range is provided, defaults to the last 90 days. Date range is capped at 730 days max.  Pass `timeIncrement=1` to also get a daily breakdown: each node gains a `daily[]` array of per-day metrics (same fields as the aggregated `metrics`) in the same call. Use `dailyLevel` (`campaign` default, or `adset` / `ad`) to choose which levels carry the series. This replaces calling the tree once per day for per-campaign daily trends. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**page** | Option<**i32**> | Page number (1-based) |  |[default to 1]
**limit** | Option<**i32**> | Campaigns per page |  |[default to 20]
**source** | Option<**String**> | `all` (default) returns both Zernio-created ads and those discovered from the platform's ad manager — matches the web UI's default view. Pass `zernio` to restrict to isExternal=false only. Status is NOT filtered by default — use the `status` param for that. |  |[default to all]
**platform** | Option<**String**> |  |  |
**status** | Option<[**AdStatus**](AdStatus.md)> | Filter by derived campaign status (post-aggregation) |  |
**ad_account_id** | Option<**String**> | Platform ad account ID |  |
**account_id** | Option<**String**> | Social account ID |  |
**profile_id** | Option<**String**> | Profile ID |  |
**campaign_id** | Option<**String**> | Restrict the tree to a single campaign by its platform campaign id (the id the platform assigns, e.g. Meta's numeric campaign id). Filters the campaign set itself, so it works regardless of account size and pagination — pass this when you already hold a campaign id instead of paging the tree to find it. Mirrors the `campaignId` filter on GET /v1/ads. |  |
**from_date** | Option<**String**> | Start of the METRICS date range (YYYY-MM-DD). Affects only the spend/impression numbers overlaid on each node, NOT which campaigns are returned. Defaults to 90 days ago. |  |
**to_date** | Option<**String**> | End of metrics date range (YYYY-MM-DD). Defaults to today. Max 730-day range. |  |
**sort** | Option<**String**> | Campaign-level sort order. `newest` (default) / `oldest` order by the campaign's newest-ad createdAt. `spend_desc` / `spend_asc` order by aggregated spend in the requested date range; campaigns with no spend land at the end. |  |[default to newest]
**time_increment** | Option<**i32**> | Set to `1` to also return a daily breakdown. Mirrors Meta Insights' `time_increment=1`: each node gains a `daily[]` array of per-day metrics (same fields as the aggregated `metrics`) alongside the range total, so you get per-entity daily trends in ONE call instead of calling the tree once per day. Only `1` (daily) is supported. The daily series covers the same date range and uses the same source data as `metrics`. See `dailyLevel` to control which levels carry it. |  |
**daily_level** | Option<**String**> | Which tree levels get the `daily[]` series when `timeIncrement=1`. `campaign` (default) attaches it on campaign nodes only — the common per-campaign-trend case, and the smallest payload. `adset` adds it on ad sets too; `ad` adds it on every ad in `ads[]` as well (heaviest — a long range × up to 100 ads per ad set). Scope with `campaignId` to keep `ad`-level responses small. Ignored when `timeIncrement` is unset. |  |[default to campaign]

### Return type

[**models::GetAdTree200Response**](getAdTree_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ads_timeline

> models::GetAdsTimeline200Response get_ads_timeline(account_id, ad_account_id, from_date, to_date, platform)
Get daily account metrics

Returns daily aggregate metrics across all ads in a SocialAccount as a single time series — one row per calendar day in the requested range. Use this for dashboards that draw a daily-spend or daily-conversions chart, instead of calling `/v1/ads/tree` once per day.  `accountId` is required. The lookup is sibling-expanded so passing the `metaads` ID also includes ads under the linked `facebook` / `instagram` posting account (and vice-versa) — same convention as `/v1/ads/tree` and `/v1/ads`.  Date range defaults to the last 90 days. Capped at 730 days. Ranges older than the ingested history return a `202` immediately with the covered part and `backfillPending: true` while the rest is backfilled in the background; repeat the request shortly until it returns 200 with full data. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Social account ID. Sibling-expanded to its linked posting↔ads pair. | [required] |
**ad_account_id** | Option<**String**> | Optional platform-native ad account ID (e.g. Meta `act_…`, TikTok advertiser ID). Use when the connection wraps multiple platform ad accounts and the chart should show one only. Note: rows ingested before 2026-05-13 don't carry this column; the recurring 7-day re-sync repopulates them naturally. |  |
**from_date** | Option<**String**> | Inclusive start of metrics range (YYYY-MM-DD). Defaults to 90 days ago. |  |
**to_date** | Option<**String**> | Inclusive end of metrics range (YYYY-MM-DD). Defaults to today. Max 730-day range. |  |
**platform** | Option<**String**> | Restrict to one platform. |  |

### Return type

[**models::GetAdsTimeline200Response**](getAdsTimeline_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ad_campaigns

> models::ListAdCampaigns200Response list_ad_campaigns(page, limit, source, platform, status, ad_account_id, account_id, profile_id, from_date, to_date)
List campaigns

Returns campaigns as virtual aggregations over ad documents grouped by platform campaign ID. Metrics (spend, impressions, clicks, etc.) are summed across all ads in each campaign. Campaign status is derived from child ad statuses (active > pending_review > paused > error > completed > cancelled > rejected). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**page** | Option<**i32**> | Page number (1-based) |  |[default to 1]
**limit** | Option<**i32**> |  |  |[default to 20]
**source** | Option<**String**> | `all` (default) returns both Zernio-created ads and those discovered from the platform's ad manager — matches the web UI's default view. Pass `zernio` to restrict to isExternal=false only. Status is NOT filtered by default — use the `status` param for that. |  |[default to all]
**platform** | Option<**String**> |  |  |
**status** | Option<[**AdStatus**](AdStatus.md)> | Filter by derived campaign status (post-aggregation) |  |
**ad_account_id** | Option<**String**> | Platform ad account ID (e.g. act_123 for Meta) |  |
**account_id** | Option<**String**> | Social account ID |  |
**profile_id** | Option<**String**> | Profile ID |  |
**from_date** | Option<**String**> | Start of metrics date range (YYYY-MM-DD, inclusive). Defaults to 90 days ago when both date params are omitted. |  |
**to_date** | Option<**String**> | End of metrics date range (YYYY-MM-DD, inclusive). Defaults to today. Max 730-day range. |  |

### Return type

[**models::ListAdCampaigns200Response**](listAdCampaigns_200_response.md)

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


## update_ad_campaign

> models::UpdateAdCampaign200Response update_ad_campaign(campaign_id, update_ad_campaign_request)
Update a campaign

Campaign-level edits. At least one of `budget`, `bidStrategy`, `name` or `platformSpecificData` is required.  - `budget` updates the CBO (Campaign Budget Optimization) budget. For ABO campaigns   (where the budget lives on the ad set), use PUT /v1/ads/ad-sets/{adSetId} instead — this endpoint   will return 409 with code BUDGET_LEVEL_MISMATCH. - `bidStrategy` sets the campaign-level default bid strategy. Per Meta's spec, `bid_amount` and   `bid_constraints` do NOT exist at the campaign level — pass them via PUT /v1/ads/ad-sets/{adSetId}. - `platformSpecificData.spendCap` (Meta only) sets the campaign's lifetime spend cap, in the ad   account's currency.  Meta-only for now. Other platforms return 501 Not Implemented. 

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

Updates the status of all ads in a campaign. Makes one platform API call (not per-ad) since status cascades through the campaign hierarchy. Ads in terminal statuses (rejected, completed, cancelled) are automatically skipped. 

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


## update_ad_set

> models::UpdateAdSet200Response update_ad_set(ad_set_id, update_ad_set_request)
Update an ad set

Ad-set-level writes. Use this for ABO budget updates, ad-set-scoped pause/resume, bid-strategy edits, and Meta-only post-launch delivery settings via `platformSpecificData`. At least one updatable field is required.  Bid strategy compatibility (per Meta's spec): - `LOWEST_COST_WITHOUT_CAP`: no `bidAmount`, no `roasAverageFloor`. - `LOWEST_COST_WITH_BID_CAP` / `COST_CAP`: `bidAmount` REQUIRED (whole currency units). - `LOWEST_COST_WITH_MIN_ROAS`: `roasAverageFloor` REQUIRED (decimal multiplier, e.g. 2.0 = 2.0x ROAS).  Delivery settings are validated by Meta against the campaign objective; incompatible combinations (e.g. a billingEvent the optimization goal doesn't allow) surface as 400s from Meta.  When updating `budget` on an ABO campaign: if the parent campaign is CBO, the response is 409 with code BUDGET_LEVEL_MISMATCH — route to PUT /v1/ads/campaigns/{campaignId} instead. 

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

Ad-set-scoped pause/resume (doesn't touch sibling ad sets). Thin wrapper over PUT /v1/ads/ad-sets/{adSetId} for callers that only want the status toggle and prefer a symmetric URL to /v1/ads/campaigns/{campaignId}/status. 

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

> models::UpdateAdStatus200Response update_ad_status(ad_id, update_ad_status_request)
Pause or resume a single ad

Ad-scoped pause/resume — touches ONLY this ad, never its parent ad set or campaign (so sibling ads keep running). Thin wrapper over the `status` field of PUT /v1/ads/{adId}, for callers that want a URL symmetric to /v1/ads/campaigns/{campaignId}/status and /v1/ads/ad-sets/{adSetId}/status.  `{adId}` accepts the same identifier dialects as GET/PUT /v1/ads/{adId} (Zernio hex `_id`, Meta numeric `platformAdId`, or the creative's effective story/media IDs). `platform` is inferred from the ad, so it's not required in the body. Ads in terminal statuses (rejected, completed, cancelled) and no-op flips (already in the target state) are skipped. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_id** | **String** | Zernio `_id` (hex), Meta `platformAdId` (numeric), or one of the creative's effective story/media IDs. | [required] |
**update_ad_status_request** | [**UpdateAdStatusRequest**](UpdateAdStatusRequest.md) |  | [required] |

### Return type

[**models::UpdateAdStatus200Response**](updateAdStatus_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

