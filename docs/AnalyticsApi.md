# \AnalyticsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_analytics**](AnalyticsApi.md#get_analytics) | **GET** /v1/analytics | Get post analytics
[**get_best_time_to_post**](AnalyticsApi.md#get_best_time_to_post) | **GET** /v1/analytics/best-time | Get best times to post
[**get_content_decay**](AnalyticsApi.md#get_content_decay) | **GET** /v1/analytics/content-decay | Get content performance decay
[**get_daily_metrics**](AnalyticsApi.md#get_daily_metrics) | **GET** /v1/analytics/daily-metrics | Get daily aggregated metrics
[**get_facebook_page_insights**](AnalyticsApi.md#get_facebook_page_insights) | **GET** /v1/analytics/facebook/page-insights | Get Facebook Page insights
[**get_follower_stats**](AnalyticsApi.md#get_follower_stats) | **GET** /v1/accounts/follower-stats | Get follower stats
[**get_google_business_performance**](AnalyticsApi.md#get_google_business_performance) | **GET** /v1/analytics/googlebusiness/performance | Get GBP performance metrics
[**get_google_business_search_keywords**](AnalyticsApi.md#get_google_business_search_keywords) | **GET** /v1/analytics/googlebusiness/search-keywords | Get GBP search keywords
[**get_instagram_account_insights**](AnalyticsApi.md#get_instagram_account_insights) | **GET** /v1/analytics/instagram/account-insights | Get Instagram insights
[**get_instagram_demographics**](AnalyticsApi.md#get_instagram_demographics) | **GET** /v1/analytics/instagram/demographics | Get Instagram demographics
[**get_instagram_follower_history**](AnalyticsApi.md#get_instagram_follower_history) | **GET** /v1/analytics/instagram/follower-history | Get Instagram follower history
[**get_linked_in_aggregate_analytics**](AnalyticsApi.md#get_linked_in_aggregate_analytics) | **GET** /v1/accounts/{accountId}/linkedin-aggregate-analytics | Get LinkedIn aggregate stats
[**get_linked_in_org_aggregate_analytics**](AnalyticsApi.md#get_linked_in_org_aggregate_analytics) | **GET** /v1/analytics/linkedin/org-aggregate-analytics | Get LinkedIn organization page aggregate analytics
[**get_linked_in_post_analytics**](AnalyticsApi.md#get_linked_in_post_analytics) | **GET** /v1/accounts/{accountId}/linkedin-post-analytics | Get LinkedIn post stats
[**get_linked_in_post_reactions**](AnalyticsApi.md#get_linked_in_post_reactions) | **GET** /v1/accounts/{accountId}/linkedin-post-reactions | Get LinkedIn post reactions
[**get_post_timeline**](AnalyticsApi.md#get_post_timeline) | **GET** /v1/analytics/post-timeline | Get post analytics timeline
[**get_posting_frequency**](AnalyticsApi.md#get_posting_frequency) | **GET** /v1/analytics/posting-frequency | Get frequency vs engagement
[**get_tik_tok_account_insights**](AnalyticsApi.md#get_tik_tok_account_insights) | **GET** /v1/analytics/tiktok/account-insights | Get TikTok account-level insights
[**get_you_tube_channel_insights**](AnalyticsApi.md#get_you_tube_channel_insights) | **GET** /v1/analytics/youtube/channel-insights | Get YouTube channel-level insights
[**get_you_tube_daily_views**](AnalyticsApi.md#get_you_tube_daily_views) | **GET** /v1/analytics/youtube/daily-views | Get YouTube daily views
[**get_you_tube_demographics**](AnalyticsApi.md#get_you_tube_demographics) | **GET** /v1/analytics/youtube/demographics | Get YouTube demographics



## get_analytics

> models::GetAnalytics200Response get_analytics(post_id, platform, profile_id, account_id, source, from_date, to_date, limit, page, sort_by, order)
Get post analytics

Returns analytics for posts. With postId, returns a single post. Without it, returns a paginated list with overview stats. Accepts both Zernio Post IDs and External Post IDs (auto-resolved). fromDate defaults to 90 days ago if omitted, max range 366 days. Single post lookups may return 202 (sync pending) or 424 (all platforms failed). For follower stats, use /v1/accounts/follower-stats.  LinkedIn personal accounts: Analytics are only available for posts published through Zernio. LinkedIn's API only returns metrics for posts authored by the authenticated user. Organization/company page analytics work for all posts. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | Option<**String**> | Returns analytics for a single post. Accepts both Zernio Post IDs and External Post IDs. Zernio IDs are auto-resolved to External Post analytics. |  |
**platform** | Option<**String**> | Filter by platform (default \"all\") |  |
**profile_id** | Option<**String**> | Filter by profile ID (default \"all\") |  |
**account_id** | Option<**String**> | Filter by social account ID |  |
**source** | Option<**String**> | Filter by post source: late (posted via Zernio API), external (synced from platform), all (default) |  |[default to all]
**from_date** | Option<**String**> | Inclusive lower bound (YYYY-MM-DD). Defaults to 90 days ago if omitted. Max range is 366 days. |  |
**to_date** | Option<**String**> | Inclusive upper bound (YYYY-MM-DD). Defaults to today if omitted. |  |
**limit** | Option<**i32**> | Page size (default 50) |  |[default to 50]
**page** | Option<**i32**> | Page number (default 1) |  |[default to 1]
**sort_by** | Option<**String**> | Sort by date, engagement, or a specific metric |  |[default to date]
**order** | Option<**String**> | Sort order |  |[default to desc]

### Return type

[**models::GetAnalytics200Response**](getAnalytics_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_best_time_to_post

> models::GetBestTimeToPost200Response get_best_time_to_post(platform, profile_id, account_id, source)
Get best times to post

Returns the best times to post based on historical engagement data. Groups all published posts by day of week and hour (UTC), calculating average engagement per slot. Use this to auto-schedule posts at optimal times. Requires the Analytics add-on. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**platform** | Option<**String**> | Filter by platform (e.g. \"instagram\", \"tiktok\"). Omit for all platforms. |  |
**profile_id** | Option<**String**> | Filter by profile ID. Omit for all profiles. |  |
**account_id** | Option<**String**> | Filter by social account ID. Omit for all accounts. |  |
**source** | Option<**String**> | Filter by post origin. \"late\" for posts published via Zernio, \"external\" for posts imported from platforms. |  |[default to all]

### Return type

[**models::GetBestTimeToPost200Response**](getBestTimeToPost_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_content_decay

> models::GetContentDecay200Response get_content_decay(platform, profile_id, account_id, source)
Get content performance decay

Returns how engagement accumulates over time after a post is published. Each bucket shows what percentage of the post's total engagement had been reached by that time window. Useful for understanding content lifespan (e.g. \"posts reach 78% of total engagement within 24 hours\"). Requires the Analytics add-on. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**platform** | Option<**String**> | Filter by platform (e.g. \"instagram\", \"tiktok\"). Omit for all platforms. |  |
**profile_id** | Option<**String**> | Filter by profile ID. Omit for all profiles. |  |
**account_id** | Option<**String**> | Filter by social account ID. Omit for all accounts. |  |
**source** | Option<**String**> | Filter by post origin. \"late\" for posts published via Zernio, \"external\" for posts imported from platforms. |  |[default to all]

### Return type

[**models::GetContentDecay200Response**](getContentDecay_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_daily_metrics

> models::GetDailyMetrics200Response get_daily_metrics(platform, profile_id, account_id, from_date, to_date, source)
Get daily aggregated metrics

Returns daily aggregated analytics metrics and a per-platform breakdown. Each day includes post count, platform distribution, and summed metrics (impressions, reach, likes, comments, shares, saves, clicks, views). Defaults to the last 180 days. Requires the Analytics add-on. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**platform** | Option<**String**> | Filter by platform (e.g. \"instagram\", \"tiktok\"). Omit for all platforms. |  |
**profile_id** | Option<**String**> | Filter by profile ID. Omit for all profiles. |  |
**account_id** | Option<**String**> | Filter by social account ID |  |
**from_date** | Option<**String**> | Inclusive start date (ISO 8601). Defaults to 180 days ago. |  |
**to_date** | Option<**String**> | Inclusive end date (ISO 8601). Defaults to now. |  |
**source** | Option<**String**> | Filter by post origin. \"late\" for posts published via Zernio, \"external\" for posts imported from platforms. |  |[default to all]

### Return type

[**models::GetDailyMetrics200Response**](getDailyMetrics_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_facebook_page_insights

> models::InstagramAccountInsightsResponse get_facebook_page_insights(account_id, metrics, since, until, metric_type)
Get Facebook Page insights

Returns page-level Facebook insights (media views, views, post engagements, video metrics, follower counts). Response shape matches /v1/analytics/instagram/account-insights so the same client handling works across platforms.  Metric names track the current (post-November 2025) Meta Graph API. The legacy page_impressions / page_fans / page_fan_adds / page_fan_removes metrics were deprecated by Meta on November 15, 2025 and are NOT accepted by this endpoint. Use the replacements below. Because Meta did not provide direct adds/removes replacements, Zernio synthesizes followers_gained / followers_lost from the daily follower snapshotter.  Max 89 days, defaults to last 30 days. Requires the Analytics add-on. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio SocialAccount ID for the connected Facebook Page. | [required] |
**metrics** | Option<**String**> | Comma-separated list of metrics. Defaults to \"page_media_view,page_post_engagements,page_follows,followers_gained,followers_lost\".  Live Meta metrics (current names, post-Nov-2025):   - page_media_view       (replaces deprecated page_impressions)   - page_views_total   - page_post_engagements   - page_video_views   - page_video_view_time   - page_follows          (replaces deprecated page_fans)  Zernio-synthesized from daily follower snapshots (filling the Nov-2025 gap left by the page_fan_adds / page_fan_removes deprecation):   - followers_gained   - followers_lost  |  |
**since** | Option<**String**> | Start date (YYYY-MM-DD). Defaults to 30 days ago. |  |
**until** | Option<**String**> | End date (YYYY-MM-DD). Defaults to today. |  |
**metric_type** | Option<**String**> | \"total_value\" (default) returns aggregated totals only. \"time_series\" returns daily values in the \"values\" array.  |  |[default to total_value]

### Return type

[**models::InstagramAccountInsightsResponse**](InstagramAccountInsightsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_follower_stats

> models::GetFollowerStats200Response get_follower_stats(account_ids, profile_id, from_date, to_date, granularity)
Get follower stats

Returns follower count history and growth metrics for connected social accounts. Requires analytics add-on subscription. Follower counts are refreshed once per day. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_ids** | Option<**String**> | Comma-separated list of account IDs (optional, defaults to all user's accounts) |  |
**profile_id** | Option<**String**> | Filter by profile ID |  |
**from_date** | Option<**String**> | Start date in YYYY-MM-DD format (defaults to 30 days ago) |  |
**to_date** | Option<**String**> | End date in YYYY-MM-DD format (defaults to today) |  |
**granularity** | Option<**String**> | Data aggregation level |  |[default to daily]

### Return type

[**models::GetFollowerStats200Response**](getFollowerStats_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_google_business_performance

> models::GetGoogleBusinessPerformance200Response get_google_business_performance(account_id, metrics, start_date, end_date)
Get GBP performance metrics

Returns daily performance metrics for a Google Business Profile location. Metrics include impressions (Maps/Search, desktop/mobile), website clicks, call clicks, direction requests, conversations, bookings, and food orders. Data may be delayed 2-3 days. Max 18 months of historical data. Requires the Analytics add-on. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio SocialAccount ID for the Google Business Profile account. | [required] |
**metrics** | Option<**String**> | Comma-separated metric names. Defaults to all available metrics. Valid values: BUSINESS_IMPRESSIONS_DESKTOP_MAPS, BUSINESS_IMPRESSIONS_DESKTOP_SEARCH, BUSINESS_IMPRESSIONS_MOBILE_MAPS, BUSINESS_IMPRESSIONS_MOBILE_SEARCH, BUSINESS_CONVERSATIONS, BUSINESS_DIRECTION_REQUESTS, CALL_CLICKS, WEBSITE_CLICKS, BUSINESS_BOOKINGS, BUSINESS_FOOD_ORDERS, BUSINESS_FOOD_MENU_CLICKS  |  |
**start_date** | Option<**String**> | Start date (YYYY-MM-DD). Defaults to 30 days ago. Max 18 months back. |  |
**end_date** | Option<**String**> | End date (YYYY-MM-DD). Defaults to today. |  |

### Return type

[**models::GetGoogleBusinessPerformance200Response**](getGoogleBusinessPerformance_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_google_business_search_keywords

> models::GetGoogleBusinessSearchKeywords200Response get_google_business_search_keywords(account_id, start_month, end_month)
Get GBP search keywords

Returns search keywords that triggered impressions for a Google Business Profile location. Data is aggregated monthly. Keywords below a minimum impression threshold set by Google are excluded. Max 18 months of historical data. Requires the Analytics add-on. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio SocialAccount ID for the Google Business Profile account. | [required] |
**start_month** | Option<**String**> | Start month (YYYY-MM). Defaults to 3 months ago. |  |
**end_month** | Option<**String**> | End month (YYYY-MM). Defaults to current month. |  |

### Return type

[**models::GetGoogleBusinessSearchKeywords200Response**](getGoogleBusinessSearchKeywords_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_instagram_account_insights

> models::InstagramAccountInsightsResponse get_instagram_account_insights(account_id, metrics, since, until, metric_type, breakdown)
Get Instagram insights

Returns account-level Instagram insights such as reach, views, accounts engaged, and total interactions. These metrics reflect the entire account's performance across all content surfaces (feed, stories, explore, profile), and are fundamentally different from post-level metrics. Data may be delayed up to 48 hours. Max 90 days, defaults to last 30 days. Requires the Analytics add-on. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio SocialAccount ID for the Instagram account | [required] |
**metrics** | Option<**String**> | Comma-separated list of metrics. Defaults to \"reach,views,accounts_engaged,total_interactions\". Valid metrics: reach, views, accounts_engaged, total_interactions, comments, likes, saves, shares, replies, reposts, follows_and_unfollows, profile_links_taps. Note: only \"reach\" supports metricType=time_series. All other metrics (including follows_and_unfollows) are total_value only. This is an Instagram Graph API limitation, not a Zernio limitation - the IG API does not return time-series data for these metrics. For a daily running follower count, use /v1/analytics/instagram/follower-history instead.  |  |
**since** | Option<**String**> | Start date (YYYY-MM-DD). Defaults to 30 days ago. |  |
**until** | Option<**String**> | End date (YYYY-MM-DD). Defaults to today. |  |
**metric_type** | Option<**String**> | \"total_value\" (default) returns aggregated totals and supports breakdowns. \"time_series\" returns daily values but only works with the \"reach\" metric.  |  |[default to total_value]
**breakdown** | Option<**String**> | Breakdown dimension (only valid with metricType=total_value). Valid values depend on the metric: media_product_type, follow_type, follower_type, contact_button_type.  |  |

### Return type

[**models::InstagramAccountInsightsResponse**](InstagramAccountInsightsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_instagram_demographics

> models::InstagramDemographicsResponse get_instagram_demographics(account_id, metric, breakdown, timeframe)
Get Instagram demographics

Returns audience demographic insights for an Instagram account, broken down by age, city, country, and/or gender. Requires at least 100 followers. Returns top 45 entries per dimension. Data may be delayed up to 48 hours. Requires the Analytics add-on. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio SocialAccount ID for the Instagram account | [required] |
**metric** | Option<**String**> | \"follower_demographics\" for follower audience data, or \"engaged_audience_demographics\" for engaged viewers.  |  |[default to follower_demographics]
**breakdown** | Option<**String**> | Comma-separated list of demographic dimensions: age, city, country, gender. Defaults to all four if omitted.  |  |
**timeframe** | Option<**String**> | Time period for demographic data. Defaults to \"this_month\".  |  |[default to this_month]

### Return type

[**models::InstagramDemographicsResponse**](InstagramDemographicsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_instagram_follower_history

> models::InstagramAccountInsightsResponse get_instagram_follower_history(account_id, metrics, since, until, metric_type)
Get Instagram follower history

Returns a daily running Instagram follower count time series, served from Zernio's cross-platform daily snapshotter. Exists because Meta removed follower_count from the /insights endpoint in Graph API v22+ and never exposed a historical daily series via any public API.  Response envelope matches /v1/analytics/instagram/account-insights so the same client handling works. Max 89 days, defaults to last 30 days. Requires the Analytics add-on. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio SocialAccount ID for the Instagram account. | [required] |
**metrics** | Option<**String**> | Comma-separated list. Defaults to \"follower_count,followers_gained,followers_lost\".   - follower_count   : per-day raw follower count   - followers_gained : sum of positive daily deltas   - followers_lost   : sum of absolute negative daily deltas  |  |
**since** | Option<**String**> | Start date (YYYY-MM-DD). Defaults to 30 days ago. |  |
**until** | Option<**String**> | End date (YYYY-MM-DD). Defaults to today. |  |
**metric_type** | Option<**String**> | \"total_value\" returns aggregated totals (latest for follower_count, sum for gained/lost). \"time_series\" returns per-day values in the \"values\" array.  |  |[default to total_value]

### Return type

[**models::InstagramAccountInsightsResponse**](InstagramAccountInsightsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_linked_in_aggregate_analytics

> models::GetLinkedInAggregateAnalytics200Response get_linked_in_aggregate_analytics(account_id, aggregation, start_date, end_date, metrics)
Get LinkedIn aggregate stats

Returns aggregate analytics across all posts for a LinkedIn personal account. Only includes posts published through Zernio (LinkedIn API limitation). Org accounts should use /v1/analytics instead. Requires r_member_postAnalytics scope. Saves (POST_SAVE) and sends (POST_SEND) are available for personal accounts; organization pages always return 0 for these two metrics because LinkedIn does not expose them on the organization analytics endpoint.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The ID of the LinkedIn personal account | [required] |
**aggregation** | Option<**String**> | TOTAL (default, lifetime totals) or DAILY (time series). MEMBERS_REACHED not available with DAILY. |  |[default to TOTAL]
**start_date** | Option<**String**> | Start date (YYYY-MM-DD). If omitted, returns lifetime analytics. |  |
**end_date** | Option<**String**> | End date (YYYY-MM-DD, exclusive). Defaults to today if omitted. |  |
**metrics** | Option<**String**> | Comma-separated metrics: IMPRESSION, MEMBERS_REACHED, REACTION, COMMENT, RESHARE, POST_SAVE, POST_SEND. Omit for all. |  |

### Return type

[**models::GetLinkedInAggregateAnalytics200Response**](getLinkedInAggregateAnalytics_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_linked_in_org_aggregate_analytics

> models::InstagramAccountInsightsResponse get_linked_in_org_aggregate_analytics(account_id, metrics, since, until, metric_type)
Get LinkedIn organization page aggregate analytics

Returns aggregate analytics for a LinkedIn organization page. Parallel to /v1/accounts/{id}/linkedin-aggregate-analytics (which handles personal accounts only). Backed by LinkedIn's organizationalEntityShareStatistics, organizationalEntityFollowerStatistics, and organizationPageStatistics endpoints.  Response shape matches /v1/analytics/instagram/account-insights. Max 89 days, defaults to last 30 days. Requires the Analytics add-on.  Scope requirements: r_organization_social, r_organization_followers, and r_organization_admin must all be present on the account. Accounts connected before these scopes were included in the OAuth flow will return 412 with a reauth hint.  Enforced by this endpoint:   - Page-view metrics accept only metricType=total_value (LinkedIn omits per-day     segmentation even when the API is called with DAY granularity, so a time-series     response would be meaningless).   - Date range capped at 89 days.  LinkedIn-side platform limits (not re-enforced here, but worth knowing for larger ranges in a future release):   - Follower stats: rolling 12-month window, end must be no later than 2 days ago.   - Share stats: rolling 12-month window. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio SocialAccount ID for the LinkedIn organization account. | [required] |
**metrics** | Option<**String**> | Comma-separated list. Defaults to \"impressions,clicks,engagement_rate,organic_followers_gained,followers_gained,followers_lost\".  Share statistics (support both total_value and time_series):   - impressions   - unique_impressions   - clicks   - likes   - comments   - shares   - engagement_rate       (0..1, LinkedIn-computed)  Follower-gain statistics (support total_value and time_series):   - organic_followers_gained   (per-day organic gains for time_series; sum of organic gains over the range for total_value)   - paid_followers_gained      (per-day paid gains for time_series; sum of paid gains over the range for total_value)  Page-view statistics (total_value ONLY - LinkedIn platform limit):   - page_views_total   - page_views_overview   - page_views_careers   - page_views_jobs   - page_views_life  Zernio-synthesized from daily follower snapshots:   - followers_gained   - followers_lost  |  |
**since** | Option<**String**> | Start date (YYYY-MM-DD). Defaults to 30 days ago. |  |
**until** | Option<**String**> | End date (YYYY-MM-DD). Defaults to today. |  |
**metric_type** | Option<**String**> |  |  |[default to total_value]

### Return type

[**models::InstagramAccountInsightsResponse**](InstagramAccountInsightsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_linked_in_post_analytics

> models::GetLinkedInPostAnalytics200Response get_linked_in_post_analytics(account_id, urn)
Get LinkedIn post stats

Returns analytics for a specific LinkedIn post by URN. Works for both personal and organization accounts. Saves and sends are only populated for personal accounts (LinkedIn does not expose these metrics on the organization analytics endpoint).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The ID of the LinkedIn account | [required] |
**urn** | **String** | The LinkedIn post URN | [required] |

### Return type

[**models::GetLinkedInPostAnalytics200Response**](getLinkedInPostAnalytics_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_linked_in_post_reactions

> models::GetLinkedInPostReactions200Response get_linked_in_post_reactions(account_id, urn, limit, cursor)
Get LinkedIn post reactions

Returns individual reactions for a specific LinkedIn post, including reactor profiles (name, headline/job title, profile picture, profile URL, reaction type). Only works for organization/company page accounts. LinkedIn restricts reaction data for personal profiles (r_member_social_feed is a closed permission). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The ID of the LinkedIn organization account | [required] |
**urn** | **String** | The LinkedIn post URN | [required] |
**limit** | Option<**i32**> | Maximum number of reactions to return per page |  |[default to 25]
**cursor** | Option<**String**> | Offset-based pagination start index |  |

### Return type

[**models::GetLinkedInPostReactions200Response**](getLinkedInPostReactions_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_post_timeline

> models::GetPostTimeline200Response get_post_timeline(post_id, from_date, to_date)
Get post analytics timeline

Returns a daily timeline of analytics metrics for a specific post, showing how impressions, likes, and other metrics evolved day-by-day since publishing. Each row represents one day of data per platform. For multi-platform Zernio posts, returns separate rows for each platform. Requires the Analytics add-on. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** | The post to fetch timeline for. Accepts an ExternalPost ID, a platformPostId, or a Zernio Post ID.  | [required] |
**from_date** | Option<**String**> | Start of date range (ISO 8601). Defaults to 90 days ago. |  |
**to_date** | Option<**String**> | End of date range (ISO 8601). Defaults to now. |  |

### Return type

[**models::GetPostTimeline200Response**](getPostTimeline_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_posting_frequency

> models::GetPostingFrequency200Response get_posting_frequency(platform, profile_id, account_id, source)
Get frequency vs engagement

Returns the correlation between posting frequency (posts per week) and engagement rate, broken down by platform. Helps find the optimal posting cadence for each platform. Each row represents a specific (platform, posts_per_week) combination with the average engagement rate observed across all weeks matching that frequency. Requires the Analytics add-on. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**platform** | Option<**String**> | Filter by platform (e.g. \"instagram\", \"tiktok\"). Omit for all platforms. |  |
**profile_id** | Option<**String**> | Filter by profile ID. Omit for all profiles. |  |
**account_id** | Option<**String**> | Filter by social account ID. Omit for all accounts. |  |
**source** | Option<**String**> | Filter by post origin. \"late\" for posts published via Zernio, \"external\" for posts imported from platforms. |  |[default to all]

### Return type

[**models::GetPostingFrequency200Response**](getPostingFrequency_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_tik_tok_account_insights

> models::InstagramAccountInsightsResponse get_tik_tok_account_insights(account_id, metrics, since, until, metric_type)
Get TikTok account-level insights

Returns account-level TikTok insights from /v2/user/info/ (live) plus historical time series joined from Zernio's daily snapshotter (AccountStats).  Response shape matches /v1/analytics/instagram/account-insights. Max 89 days, defaults to last 30 days. Requires the Analytics add-on and the user.info.stats scope on the account (412 if missing).  Scope intentionally narrow. TikTok's public API exposes only the four counter metrics below. The deep metrics that live in TikTok Studio are NOT available on any public TikTok API, even for Business accounts:   - profile_views   - account-level impressions / reach   - follower inflow / outflow breakdown   - video watch time, average watch time, full-watched rate   - impression_sources (FYP / Following / Hashtag / Search / Personal profile)  TikTok's Research API doesn't expose those fields either, and is restricted to non-commercial academic use per TikTok's eligibility policy. There is no public API workaround. Post-level metrics (views, likes, comments, shares per video) are available via /v1/analytics?postId=... from TikTok's /v2/video/query/. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio SocialAccount ID for the TikTok account. | [required] |
**metrics** | Option<**String**> | Comma-separated list. Defaults to \"follower_count,likes_count,video_count,followers_gained,followers_lost\".  Live from /v2/user/info/ (requires user.info.stats scope):   - follower_count  (cumulative; time series joined from AccountStats)   - following_count (cumulative; time series joined from AccountStats.metadata)   - likes_count     (cumulative; time series joined from AccountStats.metadata)   - video_count     (cumulative; time series joined from AccountStats.metadata)  Zernio-synthesized:   - followers_gained  (sum of positive daily follower deltas)   - followers_lost    (sum of absolute negative daily deltas)  |  |
**since** | Option<**String**> | Start date (YYYY-MM-DD). Defaults to 30 days ago. |  |
**until** | Option<**String**> | End date (YYYY-MM-DD). Defaults to today. |  |
**metric_type** | Option<**String**> | \"total_value\" returns the latest cumulative counter value. \"time_series\" returns daily values joined from AccountStats snapshots.  |  |[default to total_value]

### Return type

[**models::InstagramAccountInsightsResponse**](InstagramAccountInsightsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_you_tube_channel_insights

> models::InstagramAccountInsightsResponse get_you_tube_channel_insights(account_id, metrics, since, until, metric_type)
Get YouTube channel-level insights

Returns channel-scoped aggregate metrics from YouTube Analytics API v2. Saves you from looping /v1/analytics/youtube/daily-views over every video when you only need channel totals.  Response shape matches /v1/analytics/instagram/account-insights so the same client handling works. Requires yt-analytics.readonly scope (412 with reauthorizeUrl if missing). Data has a 2-3 day delay (endDate is clamped accordingly). Max 89 days, defaults to last 30 days. Requires the Analytics add-on.  NOT exposed: impressions (Studio thumbnail impressions) and impressionsClickThroughRate. YouTube Analytics API v2 does not expose these for any principal type, not channel owners, not Partner Program channels, not content owners with CMS access. The only way to get them is Studio CSV export. This is a Google-side limitation. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio SocialAccount ID for the YouTube account. | [required] |
**metrics** | Option<**String**> | Comma-separated list. Defaults to \"views,estimatedMinutesWatched,subscribersGained,subscribersLost\".  Live YouTube Analytics v2 metrics:   - views   - estimatedMinutesWatched   - averageViewDuration          (ratio - weighted mean computed across days)   - subscribersGained   - subscribersLost  Zernio-synthesized from daily follower snapshots (cross-platform parity):   - followers_gained   - followers_lost  |  |
**since** | Option<**String**> | Start date (YYYY-MM-DD). Defaults to 30 days ago. |  |
**until** | Option<**String**> | End date (YYYY-MM-DD). Defaults to today. YouTube Analytics has a 2-3 day delay, so the fetch is internally clamped to 3 days ago; any requested range extending beyond that returns zero values for the tail days. The response's dateRange.until field reflects your requested value.  |  |
**metric_type** | Option<**String**> | \"total_value\" (default) returns aggregated totals. \"time_series\" returns per-day values in the \"values\" array.  |  |[default to total_value]

### Return type

[**models::InstagramAccountInsightsResponse**](InstagramAccountInsightsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_you_tube_daily_views

> models::YouTubeDailyViewsResponse get_you_tube_daily_views(video_id, account_id, start_date, end_date)
Get YouTube daily views

Returns daily view counts for a YouTube video including views, watch time, and subscriber changes. Requires yt-analytics.readonly scope (re-authorization may be needed). Data has a 2-3 day delay. Max 90 days, defaults to last 30 days. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**video_id** | **String** | The YouTube video ID (e.g., \"dQw4w9WgXcQ\") | [required] |
**account_id** | **String** | The Zernio account ID for the YouTube account | [required] |
**start_date** | Option<**String**> | Start date (YYYY-MM-DD). Defaults to 30 days ago. |  |
**end_date** | Option<**String**> | End date (YYYY-MM-DD). Defaults to 3 days ago (YouTube data latency). |  |

### Return type

[**models::YouTubeDailyViewsResponse**](YouTubeDailyViewsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_you_tube_demographics

> models::YouTubeDemographicsResponse get_you_tube_demographics(account_id, breakdown, start_date, end_date)
Get YouTube demographics

Returns audience demographic insights for a YouTube channel, broken down by age, gender, and/or country. Age and gender values are viewer percentages (0-100). Country values are view counts. Data is based on signed-in viewers only, with a 2-3 day delay. Requires the Analytics add-on. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio SocialAccount ID for the YouTube account | [required] |
**breakdown** | Option<**String**> | Comma-separated list of demographic dimensions: age, gender, country. Defaults to all three if omitted.  |  |
**start_date** | Option<**String**> | Start date in YYYY-MM-DD format. Defaults to 90 days ago.  |  |
**end_date** | Option<**String**> | End date in YYYY-MM-DD format. Defaults to 3 days ago (YouTube data latency).  |  |

### Return type

[**models::YouTubeDemographicsResponse**](YouTubeDemographicsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

