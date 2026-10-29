# \AnalyticsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cancel_tracking_window**](AnalyticsApi.md#cancel_tracking_window) | **DELETE** /v1/analytics/tracking/{windowId} | Cancel a tracking window
[**get_analytics**](AnalyticsApi.md#get_analytics) | **GET** /v1/analytics | Get post analytics
[**get_analytics_dashboard**](AnalyticsApi.md#get_analytics_dashboard) | **GET** /v1/analytics/dashboard | Get an analytics dashboard
[**get_analytics_delta**](AnalyticsApi.md#get_analytics_delta) | **GET** /v1/analytics/delta | Analytics changed since a cursor
[**get_best_time_to_post**](AnalyticsApi.md#get_best_time_to_post) | **GET** /v1/analytics/best-time | Get best times to post
[**get_content_decay**](AnalyticsApi.md#get_content_decay) | **GET** /v1/analytics/content-decay | Get content performance decay
[**get_daily_metrics**](AnalyticsApi.md#get_daily_metrics) | **GET** /v1/analytics/daily-metrics | Get daily aggregated metrics
[**get_facebook_demographics**](AnalyticsApi.md#get_facebook_demographics) | **GET** /v1/analytics/facebook/demographics | Get Facebook Page demographics
[**get_facebook_page_insights**](AnalyticsApi.md#get_facebook_page_insights) | **GET** /v1/analytics/facebook/page-insights | Get Facebook Page insights
[**get_facebook_post_earnings**](AnalyticsApi.md#get_facebook_post_earnings) | **GET** /v1/analytics/facebook/post-earnings | Get Facebook post monetization earnings
[**get_facebook_post_reactions**](AnalyticsApi.md#get_facebook_post_reactions) | **GET** /v1/accounts/{accountId}/facebook-post-reactions | Get Facebook post reactions
[**get_follower_stats**](AnalyticsApi.md#get_follower_stats) | **GET** /v1/accounts/follower-stats | Get follower stats
[**get_google_analytics_metadata**](AnalyticsApi.md#get_google_analytics_metadata) | **GET** /v1/analytics/googleanalytics/metadata | List Google Analytics (GA4) dimensions and metrics
[**get_google_business_performance**](AnalyticsApi.md#get_google_business_performance) | **GET** /v1/analytics/googlebusiness/performance | Get Google Business Profile performance metrics
[**get_google_business_search_keywords**](AnalyticsApi.md#get_google_business_search_keywords) | **GET** /v1/analytics/googlebusiness/search-keywords | Get Google Business Profile search keywords
[**get_instagram_account_insights**](AnalyticsApi.md#get_instagram_account_insights) | **GET** /v1/analytics/instagram/account-insights | Get Instagram insights
[**get_instagram_demographics**](AnalyticsApi.md#get_instagram_demographics) | **GET** /v1/analytics/instagram/demographics | Get Instagram demographics
[**get_instagram_follower_history**](AnalyticsApi.md#get_instagram_follower_history) | **GET** /v1/analytics/instagram/follower-history | Get Instagram follower history
[**get_instagram_online_followers**](AnalyticsApi.md#get_instagram_online_followers) | **GET** /v1/analytics/instagram/online-followers | Get Instagram online followers
[**get_linked_in_aggregate_analytics**](AnalyticsApi.md#get_linked_in_aggregate_analytics) | **GET** /v1/accounts/{accountId}/linkedin-aggregate-analytics | Get LinkedIn aggregate stats
[**get_linked_in_demographics**](AnalyticsApi.md#get_linked_in_demographics) | **GET** /v1/analytics/linkedin/demographics | Get LinkedIn organization follower demographics
[**get_linked_in_org_aggregate_analytics**](AnalyticsApi.md#get_linked_in_org_aggregate_analytics) | **GET** /v1/analytics/linkedin/org-aggregate-analytics | Get LinkedIn org analytics
[**get_linked_in_post_analytics**](AnalyticsApi.md#get_linked_in_post_analytics) | **GET** /v1/accounts/{accountId}/linkedin-post-analytics | Get LinkedIn post stats
[**get_linked_in_post_reactions**](AnalyticsApi.md#get_linked_in_post_reactions) | **GET** /v1/accounts/{accountId}/linkedin-post-reactions | Get LinkedIn post reactions
[**get_post_authenticity**](AnalyticsApi.md#get_post_authenticity) | **GET** /v1/posts/{postId}/authenticity | Get a post's authenticity score
[**get_post_samples**](AnalyticsApi.md#get_post_samples) | **GET** /v1/analytics/samples | Get post samples
[**get_post_timeline**](AnalyticsApi.md#get_post_timeline) | **GET** /v1/analytics/post-timeline | Get post analytics timeline
[**get_posting_frequency**](AnalyticsApi.md#get_posting_frequency) | **GET** /v1/analytics/posting-frequency | Get frequency vs engagement
[**get_tik_tok_account_insights**](AnalyticsApi.md#get_tik_tok_account_insights) | **GET** /v1/analytics/tiktok/account-insights | Get TikTok account-level insights
[**get_tracking_window**](AnalyticsApi.md#get_tracking_window) | **GET** /v1/analytics/tracking/{windowId} | Get a tracking window
[**get_you_tube_channel_insights**](AnalyticsApi.md#get_you_tube_channel_insights) | **GET** /v1/analytics/youtube/channel-insights | Get YouTube channel insights
[**get_you_tube_daily_views**](AnalyticsApi.md#get_you_tube_daily_views) | **GET** /v1/analytics/youtube/daily-views | Get YouTube daily views
[**get_you_tube_demographics**](AnalyticsApi.md#get_you_tube_demographics) | **GET** /v1/analytics/youtube/demographics | Get YouTube demographics
[**get_you_tube_video_retention**](AnalyticsApi.md#get_you_tube_video_retention) | **GET** /v1/analytics/youtube/video-retention | Get YouTube video retention curve
[**list_facebook_tagged_posts**](AnalyticsApi.md#list_facebook_tagged_posts) | **GET** /v1/accounts/{accountId}/facebook-tagged-posts | List the posts a Facebook Page is tagged in
[**list_facebook_visitor_posts**](AnalyticsApi.md#list_facebook_visitor_posts) | **GET** /v1/accounts/{accountId}/facebook-visitor-posts | List visitor posts on a Facebook Page
[**list_post_authenticity**](AnalyticsApi.md#list_post_authenticity) | **GET** /v1/analytics/authenticity | List authenticity scores
[**list_tracking_windows**](AnalyticsApi.md#list_tracking_windows) | **GET** /v1/analytics/tracking | List tracking windows
[**open_tracking_window**](AnalyticsApi.md#open_tracking_window) | **POST** /v1/analytics/tracking | Open a tracking window
[**run_google_analytics_realtime_report**](AnalyticsApi.md#run_google_analytics_realtime_report) | **POST** /v1/analytics/googleanalytics/realtime | Run a Google Analytics (GA4) realtime report
[**run_google_analytics_report**](AnalyticsApi.md#run_google_analytics_report) | **POST** /v1/analytics/googleanalytics/report | Run a Google Analytics (GA4) report
[**sync_external_posts**](AnalyticsApi.md#sync_external_posts) | **POST** /v1/posts/sync-external | Sync an external post



## cancel_tracking_window

> models::TrackingWindowResponse cancel_tracking_window(window_id)
Cancel a tracking window

Stops tracking and returns the window with its final status. A window that already completed keeps its `completed` status and its final read. A cancelled window gets no final read and fires no `post.tracking_completed` webhook. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**window_id** | **String** |  | [required] |

### Return type

[**models::TrackingWindowResponse**](TrackingWindowResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_analytics

> models::GetAnalytics200Response get_analytics(post_id, platform, profile_id, account_id, source, from_date, to_date, limit, page, sort_by, order, tags)
Get post analytics

Returns analytics for posts. With postId, returns a single post. Without it, returns a paginated list with overview stats.  - Accepts both Zernio Post IDs and External Post IDs (auto-resolved). - fromDate defaults to 90 days ago if omitted, max range 366 days. - Single post lookups may return 202 (sync pending) or 424 (all platforms failed). - For follower stats, use /v1/accounts/follower-stats.  ### LinkedIn personal accounts  Analytics are only available for posts published through Zernio. LinkedIn's API only returns metrics for posts authored by the authenticated user. Organization/company page analytics work for all posts.  ### Facebook Page stories  Stories on a connected Page, published through Zernio or natively, are collected while they are live and returned like any other post (platformPostUrl points to the story). Metrics for a story published through Zernio are available on its Zernio post ID.  Their lifetime metrics refresh about hourly, with a final reading shortly before the story expires at 24 hours. After that the values stay at that last reading.  Mapping:  - impressions = story media views (Meta stopped accepting per-story impressions in October 2026, so impressions equals views) - reach = unique story media viewers - views = story media views - likes = story reactions - comments = story replies - shares = story shares - clicks: always 0, because Meta exposes no link-click metric for stories 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | Option<**String**> | Returns analytics for a single post. Accepts both Zernio Post IDs and External Post IDs. Zernio IDs are auto-resolved to External Post analytics. |  |
**platform** | Option<**String**> | Filter by platform (default \"all\") |  |
**profile_id** | Option<**String**> | Filter by profile ID (default \"all\") |  |
**account_id** | Option<**String**> | Filter by account ID |  |
**source** | Option<**String**> | Filter by post source: late (posted via Zernio API), external (synced from platform), all (default) |  |[default to all]
**from_date** | Option<**String**> | Inclusive lower bound (YYYY-MM-DD). Defaults to 90 days ago if omitted. Max range is 366 days. |  |
**to_date** | Option<**String**> | Inclusive upper bound (YYYY-MM-DD). Defaults to today if omitted. |  |
**limit** | Option<**i32**> | Page size (default 50) |  |[default to 50]
**page** | Option<**i32**> | Page number (default 1) |  |[default to 1]
**sort_by** | Option<**String**> | Sort by date, engagement, or a specific metric. Platform-specific metrics (follows, reposts, reels_skip_rate, ig_reels_*, completion_rate, profile_views, website_clicks) sort a null value as 0. |  |[default to date]
**order** | Option<**String**> | Sort order |  |[default to desc]
**tags** | Option<**String**> | Comma-separated tags (at most 20). Lists only posts created through Zernio that carry every listed tag, matched exactly and case-sensitively. Up to 200 published posts can match within the date range; more returns 400 asking to narrow fromDate and toDate. Ignored when postId is set. |  |

### Return type

[**models::GetAnalytics200Response**](getAnalytics_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_analytics_dashboard

> models::GetAnalyticsDashboard200Response get_analytics_dashboard(from_date, to_date, profile_id, platform, compare, top_posts, recent_posts)
Get an analytics dashboard

Everything an analytics dashboard needs in one call: window totals, follower growth, a per-day series, top posts, recent posts and, optionally, the same figures for the previous period.  All dates are UTC days.  ### Daily and total metrics  Daily and total metrics use received attribution: each day holds the engagement that arrived that day, on any post. So `totals` is always the sum of `daily`.  ### Post lists  `topPosts` and `recentPosts` list posts published in the window with their lifetime metrics. A post cross-posted to several platforms appears once per platform. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**from_date** | **String** | First day of the window (YYYY-MM-DD, inclusive). | [required] |
**to_date** | **String** | Last day of the window (YYYY-MM-DD, inclusive). May equal fromDate. The window covers at most 366 days. | [required] |
**profile_id** | Option<**String**> | Profile ID, or \"all\" for every profile you can access. |  |[default to all]
**platform** | Option<**String**> | Platform to cover (e.g. \"instagram\"), or \"all\". |  |[default to all]
**compare** | Option<**String**> | Set to \"previous_period\" to also return previousTotals and previousFollowers for the window of the same length that ends the day before fromDate. |  |
**top_posts** | Option<**i32**> | How many top posts to return, ranked by engagement (likes, comments, shares and saves, the same sum as daily engagement). |  |[default to 5]
**recent_posts** | Option<**i32**> | How many of the most recently published posts to return. |  |[default to 10]

### Return type

[**models::GetAnalyticsDashboard200Response**](getAnalyticsDashboard_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_analytics_delta

> models::AnalyticsDeltaResponse get_analytics_delta(cursor, limit, platform, profile_id)
Analytics changed since a cursor

Cursor feed of the analytics snapshots that CHANGED, across every account you can read, in one paginated stream. Built for integrations that would otherwise call `GET /v1/analytics` once per connected account.  Each page carries changes from many accounts at once, so your call count scales with how much actually changed rather than with how many accounts you have.  Measured against a fleet of roughly 1,600 connected accounts: about 1,599 per-account analytics calls an hour became about 205 delta calls an hour, a 7.8x reduction.  ### Bootstrap once, then stay in sync  1. Take the cursor FIRST: call this endpoint with NO `cursor`. It answers with an empty `data` array plus the feed's current position in `nextCursor`. 2. Load your baseline from `GET /v1/analytics`, the historical endpoint. This one is a rolling 7-day change log and cannot replay history. 3. Resume from the cursor you took before the baseline.  Taking the cursor afterwards instead drops every change that lands while the baseline is loading: it is in neither the row you already read nor the feed you resume behind it.  The overlap this order creates is safe. Metrics are absolute values rather than increments, so draining it leaves every post on its newest value.  `nextCursor` is present on every response, empty pages included, so you always have something to advance with.  ### Ordering  Entries come back oldest first, in the order the feed received them. That order is NOT `syncedAt`. `syncedAt` is stamped when an account's sync cycle started, and a slow cycle writes its rows after a faster cycle that started later, so `syncedAt` can go backwards between consecutive entries.  Do not sort, filter or resume on `syncedAt`. The cursor is the only stable position, and it is opaque: pass it back verbatim, and do not parse, construct or compare cursors.  ### `hasMore: false` does not mean the feed ended  This stream has no end and `nextCursor` is never null.  - `hasMore: true`: more changes are already waiting, so call again straight away. - `hasMore: false`: you are caught up. Keep the cursor and poll again on your normal interval.  ### The newest changes settle before they are served  The feed deliberately holds back its last few seconds of writes, so that a row can never become visible behind a cursor you have already advanced past.  A read issued the instant an `analytics.synced` webhook lands will therefore often return an empty page for that account. Do not read an empty page as \"nothing changed\": poll again with the SAME cursor you last used rather than advancing.  ### Repeats inside one instant  A sync cycle occasionally records the same post twice at the same feed position. When that happens the feed delivers one of those rows, not both.  Measured over a day of production traffic, about 1.3% of rows fall in such a group and 99.4% of those groups are identical rows, so this is far more often deduplication than loss.  Metrics are absolute values rather than increments, so a later entry for the same post supersedes an earlier one.  ### Retention is 7 days  Changes older than that leave the feed. A cursor older than 6 days is rejected with a `400` (a day of margin, because expiry is lazy).  Recover the same way you bootstrapped:  1. Take a fresh cursor from a call to this endpoint with no `cursor`. 2. Re-load from `GET /v1/analytics`. 3. Resume from that cursor.  A consumer that polls at least daily never reaches this.  ### Webhook and access  Pairs with the `analytics.synced` webhook, so changes can be read on notification instead of on a timer. That event carries no cursor of its own: keep using the `nextCursor` this endpoint gave you.  Requires the same analytics access as `GET /v1/analytics`, and shares the stricter per-second rate-limit window applied to analytics endpoints. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**cursor** | Option<**String**> | Opaque cursor from a previous response's `nextCursor`. Omit it to start from now: the response is then an empty page carrying the feed's current position. Rejected with a `400` when malformed, or when older than the retention window.  |  |
**limit** | Option<**i32**> | Page size. Out-of-range values are a 400, never a silent clamp. |  |[default to 50]
**platform** | Option<**String**> | Filter to a single platform (for example \"youtube\"). Omit for every platform. |  |
**profile_id** | Option<**String**> | Filter by profile ID (default \"all\"). Must be a valid profile ID or \"all\". |  |[default to all]

### Return type

[**models::AnalyticsDeltaResponse**](AnalyticsDeltaResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_best_time_to_post

> models::GetBestTimeToPost200Response get_best_time_to_post(platform, profile_id, account_id, source)
Get best times to post

Returns the best times to post based on historical engagement data. Groups all published posts by day of week and hour (UTC), calculating average engagement per slot. Use this to auto-schedule posts at optimal times. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**platform** | Option<**String**> | Filter by platform (e.g. \"instagram\", \"tiktok\"). Omit for all platforms. |  |
**profile_id** | Option<**String**> | Filter by profile ID. Omit for all profiles. |  |
**account_id** | Option<**String**> | Filter by account ID. Omit for all accounts. |  |
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

Returns how engagement accumulates over time after a post is published. Each bucket shows what percentage of the post's total engagement had been reached by that time window. Useful for understanding content lifespan (e.g. \"posts reach 78% of total engagement within 24 hours\"). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**platform** | Option<**String**> | Filter by platform (e.g. \"instagram\", \"tiktok\"). Omit for all platforms. |  |
**profile_id** | Option<**String**> | Filter by profile ID. Omit for all profiles. |  |
**account_id** | Option<**String**> | Filter by account ID. Omit for all accounts. |  |
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

> models::GetDailyMetrics200Response get_daily_metrics(platform, profile_id, account_id, from_date, to_date, source, attribution)
Get daily aggregated metrics

Returns daily aggregated analytics metrics and a per-platform breakdown. Each day includes post count, platform distribution, and summed metrics (impressions, reach, likes, comments, shares, saves, clicks, views). Defaults to the last 180 days. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**platform** | Option<**String**> | Filter by platform (e.g. \"instagram\", \"tiktok\"). Omit for all platforms. |  |
**profile_id** | Option<**String**> | Filter by profile ID. Omit for all profiles. |  |
**account_id** | Option<**String**> | Filter by account ID |  |
**from_date** | Option<**String**> | Inclusive start date (ISO 8601). Defaults to 180 days ago. |  |
**to_date** | Option<**String**> | Inclusive end date (ISO 8601). Defaults to now. |  |
**source** | Option<**String**> | Filter by post origin. \"late\" for posts published via Zernio, \"external\" for posts imported from platforms. |  |[default to all]
**attribution** | Option<**String**> | How each post's engagement is attributed to a day.  - \"publish\" (default): sums each post's lifetime total on its publish date. - \"received\": buckets the per-day increase in engagement by the day it actually arrived (engagement-over-time), so engagement on older posts appears on the day it was gained rather than the post's publish date.  |  |[default to publish]

### Return type

[**models::GetDailyMetrics200Response**](getDailyMetrics_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_facebook_demographics

> models::GetFacebookDemographics200Response get_facebook_demographics(account_id, breakdown)
Get Facebook Page demographics

Returns the follower breakdown of a connected Facebook Page by country and/or city, from Meta's latest daily snapshot.  ### Keys  - Country keys are ISO 3166-1 alpha-2 codes. - City keys are \"City, Region, Country\" strings as Meta returns them.  ### Limits  Meta removed age and gender demographics for Pages (page_fans_gender_age) on November 15 2025 with no replacement, so only country and city are available.  Meta reports small counts at a privacy floor, so the long tail can show identical low values. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio SocialAccount ID for the Facebook account | [required] |
**breakdown** | Option<**String**> | Comma-separated list of demographic dimensions: country, city. Defaults to both if omitted.  |  |

### Return type

[**models::GetFacebookDemographics200Response**](getFacebookDemographics_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_facebook_page_insights

> models::InstagramAccountInsightsResponse get_facebook_page_insights(account_id, metrics, from_date, to_date, since, until, metric_type)
Get Facebook Page insights

Returns page-level Facebook insights (media views, views, post engagements, video metrics, follower counts). The response shape matches /v1/analytics/instagram/account-insights, so the same client handling works across platforms.  Max 89 days, defaults to last 30 days.  ### Metric names  Metric names track the current (post-November 2025) Meta Graph API. These legacy metrics were deprecated by Meta on November 15, 2025 and are NOT accepted by this endpoint:  - page_impressions - page_fans - page_fan_adds - page_fan_removes  Use the replacements below. Because Meta did not provide direct adds/removes replacements, Zernio synthesizes followers_gained / followers_lost from the daily follower snapshotter. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio SocialAccount ID for the connected Facebook Page. | [required] |
**metrics** | Option<**String**> | Comma-separated list of metrics. Defaults to \"page_media_view,page_post_engagements,page_follows,followers_gained,followers_lost\".  **Live Meta metrics** (current names, post-Nov-2025):  - page_media_view (replaces deprecated page_impressions) - page_views_total - page_post_engagements - page_video_views - page_video_view_time - page_follows (replaces deprecated page_fans)  **Zernio-synthesized** from daily follower snapshots (filling the Nov-2025 gap left by the page_fan_adds / page_fan_removes deprecation):  - followers_gained - followers_lost  **Monetization** (opt-in, not in the defaults):  - content_monetization_earnings: an object per day, always with unit \"micro_amount\" and an ISO 4217 \"currency\". - monetization_approximate_earnings: a bare number per day; unit is always \"unspecified\" and \"currency\" always null.  Each monetization metric costs its own Graph call, so requesting both adds two calls. Values are approximate and Meta restates them later. The two are on different scales and not comparable. Both keep daily \"values\" on every metricType and are never rescaled by Zernio.  Earnings are Page-level daily buckets and \"total\" is their sum. Meta does not document whether a bucket is that day's earnings or a running total, and every Page measured so far earned exactly 0.  Reconcile \"total\" against the Page's Meta export before relying on it (daily \"values\" are always returned for this).  Per-post lifetime earnings: GET /v1/analytics/facebook/post-earnings.  A Page not enrolled in monetization, or that earned nothing, returns normal daily buckets of 0 in \"metrics\" (Meta does not distinguish them), so a 0 total does NOT mean the Page is enrolled.  \"unavailableMetrics\" covers the narrower case where Meta returned no bucket at all (\"no_data\") or rejected the request; the metric is then omitted from \"metrics\" rather than reported as 0.  |  |
**from_date** | Option<**String**> | Start date (YYYY-MM-DD). Defaults to 30 days ago. |  |
**to_date** | Option<**String**> | End date (YYYY-MM-DD). Defaults to today. |  |
**since** | Option<**String**> | Alias of fromDate, kept for existing callers |  |
**until** | Option<**String**> | Alias of toDate, kept for existing callers |  |
**metric_type** | Option<**String**> | \"total_value\" (default) returns aggregated totals only. \"time_series\" returns daily values in the \"values\" array.  |  |[default to total_value]

### Return type

[**models::InstagramAccountInsightsResponse**](InstagramAccountInsightsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_facebook_post_earnings

> models::FacebookPostEarningsResponse get_facebook_post_earnings(account_id, post_id, metrics)
Get Facebook post monetization earnings

Returns lifetime monetization earnings for ONE Facebook post, read live from Meta on every request.  ### Lifetime totals only  Earnings are CUMULATIVE since the post was published, not earnings within a date range. So this endpoint takes no since/until, and the totals must not be summed across dates or across posts. Page-level daily earnings live on /v1/analytics/facebook/page-insights.  ### Zeros and missing metrics  - A post on a Page that is not enrolled in monetization, or that earned nothing, returns \"total\": 0 rather than an error: Meta does not distinguish the two. - A metric Meta returned no bucket for at all is reported in \"unavailableMetrics\" and omitted from \"metrics\", never as a 0.  Amounts are the platform's raw numbers in the stated \"unit\" and are never rescaled by Zernio.  ### Rejected parameters  These are rejected with 400:  - \"breakdown\": breakdown dimensions are not exposed. - \"since\", \"until\", \"period\", and \"metricType\": scoping this endpoint to a window is not possible.  Silently returning the lifetime total for a window would let a caller sum a year of weekly requests into a figure ~52x the post's real earnings. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio SocialAccount ID for the connected Facebook Page. | [required] |
**post_id** | **String** | The platform post ID, exactly as returned in platformAnalytics[].platformPostId by /v1/analytics: \"{pageId}_{postId}\", or the bare video ID for Reels.  | [required] |
**metrics** | Option<**String**> | Comma-separated list of monetization metrics. Defaults to both:   - content_monetization_earnings   - monetization_approximate_earnings  content_monetization_earnings always carries unit \"micro_amount\" plus an ISO 4217 \"currency\". monetization_approximate_earnings is always a bare number, so its unit is \"unspecified\" and its \"currency\" is null. The two are on different scales and are not comparable to each other. Any other metric name is rejected with 400.  |  |

### Return type

[**models::FacebookPostEarningsResponse**](FacebookPostEarningsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_facebook_post_reactions

> models::GetFacebookPostReactions200Response get_facebook_post_reactions(account_id, post_id)
Get Facebook post reactions

Returns the reaction breakdown for a Facebook Page post: a count per reaction type plus the overall total.  The whole breakdown is fetched in a single Graph call. The post analytics endpoint reports only an aggregate reaction count (surfaced there as `likes`), so use this endpoint when you need per-type counts. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The ID of the Facebook Page account | [required] |
**post_id** | **String** | The Facebook post ID | [required] |

### Return type

[**models::GetFacebookPostReactions200Response**](getFacebookPostReactions_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_follower_stats

> models::FollowerStatsResponse get_follower_stats(account_ids, profile_id, from_date, to_date, granularity, limit, cursor)
Get follower stats

Returns follower count history and growth metrics for connected accounts. Requires analytics add-on subscription. Follower counts are refreshed once per day. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_ids** | Option<**String**> | Comma-separated list of account IDs (optional, defaults to all user's accounts) |  |
**profile_id** | Option<**String**> | Filter by profile ID |  |
**from_date** | Option<**String**> | Start date in YYYY-MM-DD format (defaults to 30 days ago) |  |
**to_date** | Option<**String**> | End date in YYYY-MM-DD format (defaults to today) |  |
**granularity** | Option<**String**> | Data aggregation level |  |[default to daily]
**limit** | Option<**i32**> | Accounts per page, ordered by account id. Send it to page through accounts; the response then carries `pagination.nextCursor`. Without limit or cursor every matching account is returned. |  |
**cursor** | Option<**String**> | Opaque cursor from a previous response's `pagination.nextCursor`; returns the next page of `limit` accounts (25 when limit is omitted). A cursor we cannot parse returns 400. |  |

### Return type

[**models::FollowerStatsResponse**](FollowerStatsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_google_analytics_metadata

> models::GetGoogleAnalyticsMetadata200Response get_google_analytics_metadata(account_id)
List Google Analytics (GA4) dimensions and metrics

Every dimension and metric the connected GA4 property accepts in a report, including its custom definitions. Cached for one hour. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Zernio account ID of the Google Analytics connection. | [required] |

### Return type

[**models::GetGoogleAnalyticsMetadata200Response**](getGoogleAnalyticsMetadata_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_google_business_performance

> models::GetGoogleBusinessPerformance200Response get_google_business_performance(account_id, metrics, from_date, to_date, start_date, end_date)
Get Google Business Profile performance metrics

Returns daily performance metrics for a Google Business Profile location. Metrics include impressions (Maps/Search, desktop/mobile), website clicks, call clicks, direction requests, conversations, bookings, and food orders. Data may be delayed 2-3 days. Max 18 months of historical data. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio SocialAccount ID for the Google Business Profile account. | [required] |
**metrics** | Option<**String**> | Comma-separated metric names. Defaults to all available metrics. Valid values: BUSINESS_IMPRESSIONS_DESKTOP_MAPS, BUSINESS_IMPRESSIONS_DESKTOP_SEARCH, BUSINESS_IMPRESSIONS_MOBILE_MAPS, BUSINESS_IMPRESSIONS_MOBILE_SEARCH, BUSINESS_CONVERSATIONS, BUSINESS_DIRECTION_REQUESTS, CALL_CLICKS, WEBSITE_CLICKS, BUSINESS_BOOKINGS, BUSINESS_FOOD_ORDERS, BUSINESS_FOOD_MENU_CLICKS  |  |
**from_date** | Option<**String**> | Start date (YYYY-MM-DD). Defaults to 30 days ago. Max 18 months back. |  |
**to_date** | Option<**String**> | End date (YYYY-MM-DD). Defaults to today. |  |
**start_date** | Option<**String**> | Alias of fromDate, kept for existing callers |  |
**end_date** | Option<**String**> | Alias of toDate, kept for existing callers |  |

### Return type

[**models::GetGoogleBusinessPerformance200Response**](getGoogleBusinessPerformance_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_google_business_search_keywords

> models::GetGoogleBusinessSearchKeywords200Response get_google_business_search_keywords(account_id, start_month, end_month, page_token)
Get Google Business Profile search keywords

Returns search keywords that triggered impressions for a Google Business Profile location.  - Data is aggregated monthly. - Keywords Google reports only as below a threshold have `impressions` 0 and `impressionsThreshold` set to that threshold. - Max 18 months of historical data.  ### Paging  Returns up to 100 keywords per page. When `nextPageToken` is not null, pass it as `pageToken` with the same `startMonth` and `endMonth` to get the next page. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio SocialAccount ID for the Google Business Profile account. | [required] |
**start_month** | Option<**String**> | Start month (YYYY-MM). Defaults to 3 months ago. |  |
**end_month** | Option<**String**> | End month (YYYY-MM). Defaults to current month. |  |
**page_token** | Option<**String**> | The nextPageToken from the previous page. Valid only with the same startMonth and endMonth as the request that returned it. |  |

### Return type

[**models::GetGoogleBusinessSearchKeywords200Response**](getGoogleBusinessSearchKeywords_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_instagram_account_insights

> models::InstagramAccountInsightsResponse get_instagram_account_insights(account_id, metrics, from_date, to_date, since, until, metric_type, breakdown)
Get Instagram insights

Returns account-level Instagram insights such as reach, views, accounts engaged, and total interactions.  These metrics reflect the entire account's performance across all content surfaces (feed, stories, explore, profile), and are fundamentally different from post-level metrics.  - Data may be delayed up to 48 hours. - Max 90 days, defaults to last 30 days. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio SocialAccount ID for the Instagram account | [required] |
**metrics** | Option<**String**> | Comma-separated list of metrics. Defaults to \"reach,views,accounts_engaged,total_interactions\".  Valid metrics: reach, views, accounts_engaged, total_interactions, comments, likes, saves, shares, replies, reposts, follows_and_unfollows, profile_links_taps, profile_views, website_clicks.  Only \"reach\" supports metricType=time_series. All other metrics (including follows_and_unfollows, profile_views and website_clicks) are total_value only. This is an Instagram Graph API limitation, not a Zernio one: the IG API returns no time-series data for these metrics.  For a daily running follower count, use /v1/analytics/instagram/follower-history instead.  |  |
**from_date** | Option<**String**> | Start date (YYYY-MM-DD). Defaults to 30 days ago. |  |
**to_date** | Option<**String**> | End date (YYYY-MM-DD). Defaults to today. |  |
**since** | Option<**String**> | Alias of fromDate, kept for existing callers |  |
**until** | Option<**String**> | Alias of toDate, kept for existing callers |  |
**metric_type** | Option<**String**> | \"total_value\" (default) returns aggregated totals and supports breakdowns. \"time_series\" returns daily values but only works with the \"reach\" metric.  |  |[default to total_value]
**breakdown** | Option<**String**> | Breakdown dimension (only valid with metricType=total_value). Valid values per metric: reach and views take follow_type or media_product_type; follows_and_unfollows takes follow_type; profile_links_taps takes contact_button_type; comments, likes, saves, shares and total_interactions take media_product_type.  |  |

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

Returns audience demographic insights for an Instagram account, broken down by age, city, country, and/or gender. Requires at least 100 followers. Returns top 45 entries per dimension. Data may be delayed up to 48 hours. 

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

> models::InstagramAccountInsightsResponse get_instagram_follower_history(account_id, metrics, from_date, to_date, since, until, metric_type)
Get Instagram follower history

Returns a daily running Instagram follower count time series, served from Zernio's cross-platform daily snapshotter. Exists because Meta removed follower_count from the /insights endpoint in Graph API v22+ and never exposed a historical daily series via any public API.  Response envelope matches /v1/analytics/instagram/account-insights so the same client handling works. Max 89 days, defaults to last 30 days. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio SocialAccount ID for the Instagram account. | [required] |
**metrics** | Option<**String**> | Comma-separated list. Defaults to \"follower_count,followers_gained,followers_lost\".   - follower_count   : per-day raw follower count   - followers_gained : sum of positive daily deltas   - followers_lost   : sum of absolute negative daily deltas  |  |
**from_date** | Option<**String**> | Start date (YYYY-MM-DD). Defaults to 30 days ago. |  |
**to_date** | Option<**String**> | End date (YYYY-MM-DD). Defaults to today. |  |
**since** | Option<**String**> | Alias of fromDate, kept for existing callers |  |
**until** | Option<**String**> | Alias of toDate, kept for existing callers |  |
**metric_type** | Option<**String**> | \"total_value\" returns aggregated totals (latest for follower_count, sum for gained/lost). \"time_series\" returns per-day values in the \"values\" array.  |  |[default to total_value]

### Return type

[**models::InstagramAccountInsightsResponse**](InstagramAccountInsightsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_instagram_online_followers

> models::GetInstagramOnlineFollowers200Response get_instagram_online_followers(account_id)
Get Instagram online followers

Returns how many of an Instagram account's followers were online in each hour, for every day of the last 30 days that Meta has data for.  - Hour keys are \"0\" to \"23\" as Meta returns them. Meta does not document the timezone of the hour keys. - endTime is the end_time Meta returns for that day. - Data is delayed up to 48 hours, so the most recent days are left out until Meta fills them. - Requires at least 100 followers; for smaller accounts days is empty. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio SocialAccount ID for the Instagram account | [required] |

### Return type

[**models::GetInstagramOnlineFollowers200Response**](getInstagramOnlineFollowers_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_linked_in_aggregate_analytics

> models::GetLinkedInAggregateAnalytics200Response get_linked_in_aggregate_analytics(account_id, aggregation, from_date, to_date, start_date, end_date, metrics)
Get LinkedIn aggregate stats

Returns aggregate analytics across all posts for a LinkedIn personal account. Requires r_member_postAnalytics scope.  Covers every post authored by the member, whether or not it was published through Zernio (LinkedIn aggregates by member, not by post). Org accounts should use /v1/analytics instead.  Saves (POST_SAVE) and sends (POST_SEND) are available for personal accounts. Organization pages always return 0 for these two metrics because LinkedIn does not expose them on the organization analytics endpoint. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The ID of the LinkedIn personal account | [required] |
**aggregation** | Option<**String**> | TOTAL (default, lifetime totals) or DAILY (time series). MEMBERS_REACHED not available with DAILY. |  |[default to TOTAL]
**from_date** | Option<**String**> | Start date (YYYY-MM-DD). If omitted, returns lifetime analytics. |  |
**to_date** | Option<**String**> | End date (YYYY-MM-DD, exclusive). Defaults to today if omitted. |  |
**start_date** | Option<**String**> | Alias of fromDate, kept for existing callers |  |
**end_date** | Option<**String**> | Alias of toDate, kept for existing callers |  |
**metrics** | Option<**String**> | Comma-separated metrics: IMPRESSION, MEMBERS_REACHED, REACTION, COMMENT, RESHARE, POST_SAVE, POST_SEND. Omit for all. |  |

### Return type

[**models::GetLinkedInAggregateAnalytics200Response**](getLinkedInAggregateAnalytics_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_linked_in_demographics

> models::GetLinkedInDemographics200Response get_linked_in_demographics(account_id, breakdown)
Get LinkedIn organization follower demographics

Returns the lifetime follower breakdown of a connected LinkedIn organization page by job function, seniority, industry and company size.  ### Labels  - Function, seniority and industry are labelled with LinkedIn's standardized names (English) and keep the LinkedIn URN in `id`. - Company size is labelled as a range such as `2-10` or `10001+`.  LinkedIn returns at most the top 100 values per breakdown and leaves out followers whose profile lacks that field, so a breakdown does not add up to the follower count.  ### Requirements  - Organization accounts only: a personal LinkedIn account answers 400 `personal_account_not_supported`. - Requires the r_organization_social, r_organization_followers and r_organization_admin scopes (412 otherwise). - Requires the Analytics add-on. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio SocialAccount ID of the LinkedIn organization account | [required] |
**breakdown** | Option<**String**> | Comma-separated list of demographic dimensions: function, seniority, industry, company_size. Defaults to all four if omitted.  |  |

### Return type

[**models::GetLinkedInDemographics200Response**](getLinkedInDemographics_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_linked_in_org_aggregate_analytics

> models::InstagramAccountInsightsResponse get_linked_in_org_aggregate_analytics(account_id, metrics, from_date, to_date, since, until, metric_type)
Get LinkedIn org analytics

Returns aggregate analytics for a LinkedIn organization page. Parallel to /v1/accounts/{id}/linkedin-aggregate-analytics (which handles personal accounts only). Backed by LinkedIn's organizationalEntityShareStatistics, organizationalEntityFollowerStatistics, and organizationPageStatistics endpoints.  Response shape matches /v1/analytics/instagram/account-insights. Max 89 days, defaults to last 30 days.  Scope requirements: r_organization_social, r_organization_followers, and r_organization_admin must all be present on the account. Accounts connected before these scopes were included in the OAuth flow will return 412 with a reauth hint.  Enforced by this endpoint:   - Page-view metrics accept only metricType=total_value (LinkedIn omits per-day     segmentation even when the API is called with DAY granularity, so a time-series     response would be meaningless).   - Date range capped at 89 days.  LinkedIn-side platform limits (not re-enforced here, but worth knowing for larger ranges in a future release):   - Follower stats: rolling 12-month window, end must be no later than 2 days ago.   - Share stats: rolling 12-month window. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio SocialAccount ID for the LinkedIn organization account. | [required] |
**metrics** | Option<**String**> | Comma-separated list. Defaults to \"impressions,clicks,engagement_rate,organic_followers_gained,followers_gained,followers_lost\".  Share statistics (support both total_value and time_series):   - impressions   - unique_impressions   - clicks   - likes   - comments   - shares   - engagement_rate       (0..1, LinkedIn-computed)  Follower-gain statistics (support total_value and time_series):   - organic_followers_gained   (per-day organic gains for time_series; sum of organic gains over the range for total_value)   - paid_followers_gained      (per-day paid gains for time_series; sum of paid gains over the range for total_value)  Page-view statistics (total_value ONLY - LinkedIn platform limit):   - page_views_total   - page_views_overview   - page_views_careers   - page_views_jobs   - page_views_life  Zernio-synthesized from daily follower snapshots:   - followers_gained   - followers_lost  |  |
**from_date** | Option<**String**> | Start date (YYYY-MM-DD). Defaults to 30 days ago. |  |
**to_date** | Option<**String**> | End date (YYYY-MM-DD). Defaults to today. |  |
**since** | Option<**String**> | Alias of fromDate, kept for existing callers |  |
**until** | Option<**String**> | Alias of toDate, kept for existing callers |  |
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
**cursor** | Option<**i32**> | Offset-based pagination start index |  |[default to 0]

### Return type

[**models::GetLinkedInPostReactions200Response**](getLinkedInPostReactions_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_post_authenticity

> models::PostAuthenticity get_post_authenticity(post_id)
Get a post's authenticity score

Returns Zernio's authenticity score for a post: an integer from 0 to 100 where higher means the view pattern looks more like organic viewing.  The score is ours. It is computed only from the verified samples we fetched from the platform, never from anything the creator or caller reported.  - `reasons` lists each factor that lowered it with its weight in points. - `confidence` (0 to 1) says how much data the score rests on.  A stored score newer than 30 minutes is returned as is, otherwise it is recomputed. The `post.authenticity_changed` webhook fires when a score crosses 40. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** | An external post id, a platform post id or a Zernio post id. | [required] |

### Return type

[**models::PostAuthenticity**](PostAuthenticity.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_post_samples

> models::GetPostSamples200Response get_post_samples(post_id, from_date, to_date, limit)
Get post samples

Returns the raw readings behind a post's numbers, oldest first.  Each sample is one analytics sync: the views and engagement as the platform reported them at `syncedAt`. Zernio only stores what it fetched from the platform, so nothing here was self-reported.  ### Null values  - `shares` and `saves` are null on platforms that do not return that counter, which is different from a real zero. - `watchSeconds` and `completionRate` are null when the platform gives no watch signal. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** | The post to read samples for. Accepts an external post id, a platform post id or a Zernio post id. | [required] |
**from_date** | Option<**String**> | Earliest sample to return (ISO 8601). |  |
**to_date** | Option<**String**> | Latest sample to return (ISO 8601). |  |
**limit** | Option<**i32**> | Maximum number of samples. |  |[default to 500]

### Return type

[**models::GetPostSamples200Response**](getPostSamples_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_post_timeline

> models::GetPostTimeline200Response get_post_timeline(post_id, from_date, to_date)
Get post analytics timeline

Returns a daily timeline of analytics metrics for a specific post, showing how impressions, likes, and other metrics evolved day-by-day since publishing. Each row represents one day of data per platform. For multi-platform Zernio posts, returns separate rows for each platform. 

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

Returns the correlation between posting frequency (posts per week) and engagement rate, broken down by platform. Helps find the optimal posting cadence for each platform. Each row represents a specific (platform, posts_per_week) combination with the average engagement rate observed across all weeks matching that frequency. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**platform** | Option<**String**> | Filter by platform (e.g. \"instagram\", \"tiktok\"). Omit for all platforms. |  |
**profile_id** | Option<**String**> | Filter by profile ID. Omit for all profiles. |  |
**account_id** | Option<**String**> | Filter by account ID. Omit for all accounts. |  |
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

> models::InstagramAccountInsightsResponse get_tik_tok_account_insights(account_id, metrics, from_date, to_date, since, until, metric_type)
Get TikTok account-level insights

Returns account-level TikTok insights from /v2/user/info/ (live) plus historical time series joined from Zernio's daily snapshotter (AccountStats).  - Response shape matches /v1/analytics/instagram/account-insights. - Max 89 days, defaults to last 30 days. - Requires the user.info.stats scope on the account (412 if missing).  ### Why the scope is narrow  This ACCOUNT-level endpoint intentionally exposes only the four counter metrics below. These account-level figures are not on any public TikTok API, for any account type:  - account-level impressions / reach - follower inflow / outflow breakdown - account-level watch time and audience demographics  TikTok's Research API doesn't expose them either, and is restricted to non-commercial academic use per TikTok's eligibility policy.  ### Per-video metrics  PER-VIDEO is a different story on the Business lane. An account connected through the TikTok for Business app reports these per video on GET /v1/analytics?postId=...:  - profile views, website clicks, follows - full-watched rate, watch time - impression sources, viewer types and viewer countries  They arrive roughly 24-48h after publishing and only for posts active in the last 7 days.  Accounts on the original TikTok integration get the basic counters there (views, likes, comments, shares) and zeros for the rest. They must reconnect through the Business app. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio SocialAccount ID for the TikTok account. | [required] |
**metrics** | Option<**String**> | Comma-separated list. Defaults to \"follower_count,likes_count,video_count,followers_gained,followers_lost\".  Live from /v2/user/info/ (requires user.info.stats scope):   - follower_count  (cumulative; time series joined from AccountStats)   - following_count (cumulative; time series joined from AccountStats.metadata)   - likes_count     (cumulative; time series joined from AccountStats.metadata)   - video_count     (cumulative; time series joined from AccountStats.metadata)  Zernio-synthesized:   - followers_gained  (sum of positive daily follower deltas)   - followers_lost    (sum of absolute negative daily deltas)  |  |
**from_date** | Option<**String**> | Start date (YYYY-MM-DD). Defaults to 30 days ago. |  |
**to_date** | Option<**String**> | End date (YYYY-MM-DD). Defaults to today. |  |
**since** | Option<**String**> | Alias of fromDate, kept for existing callers |  |
**until** | Option<**String**> | Alias of toDate, kept for existing callers |  |
**metric_type** | Option<**String**> | \"total_value\" returns the latest cumulative counter value. \"time_series\" returns daily values joined from AccountStats snapshots.  |  |[default to total_value]

### Return type

[**models::InstagramAccountInsightsResponse**](InstagramAccountInsightsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_tracking_window

> models::TrackingWindowResponse get_tracking_window(window_id)
Get a tracking window

Returns one tracking window with the latest verified numbers we read from the platform. Once the window has completed, `finalReadAt` and `completionReason` say how it closed. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**window_id** | **String** |  | [required] |

### Return type

[**models::TrackingWindowResponse**](TrackingWindowResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_you_tube_channel_insights

> models::InstagramAccountInsightsResponse get_you_tube_channel_insights(account_id, metrics, from_date, to_date, since, until, metric_type)
Get YouTube channel insights

Returns channel-scoped aggregate metrics from YouTube Analytics API v2. Saves you from looping /v1/analytics/youtube/daily-views over every video when you only need channel totals.  Response shape matches /v1/analytics/instagram/account-insights so the same client handling works. Requires yt-analytics.readonly scope (412 with reauthorizeUrl if missing). Data has a 2-3 day delay (endDate is clamped accordingly). Max 89 days, defaults to last 30 days.  NOT exposed: impressions (Studio thumbnail impressions) and impressionsClickThroughRate. YouTube Analytics API v2 does not expose these for any principal type, not channel owners, not Partner Program channels, not content owners with CMS access. The only way to get them is Studio CSV export. This is a Google-side limitation. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio SocialAccount ID for the YouTube account. | [required] |
**metrics** | Option<**String**> | Comma-separated list. Defaults to \"views,estimatedMinutesWatched,subscribersGained,subscribersLost\".  Live YouTube Analytics v2 metrics:   - views   - estimatedMinutesWatched   - averageViewDuration          (ratio - weighted mean computed across days)   - subscribersGained   - subscribersLost  Zernio-synthesized from daily follower snapshots (cross-platform parity):   - followers_gained   - followers_lost  |  |
**from_date** | Option<**String**> | Start date (YYYY-MM-DD). Defaults to 30 days ago. |  |
**to_date** | Option<**String**> | End date (YYYY-MM-DD). Defaults to today. YouTube Analytics has a 2-3 day delay, so the fetch is internally clamped to 3 days ago; any requested range extending beyond that returns zero values for the tail days. The response's dateRange.until field reflects your requested value.  |  |
**since** | Option<**String**> | Alias of fromDate, kept for existing callers |  |
**until** | Option<**String**> | Alias of toDate, kept for existing callers |  |
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

> models::YouTubeDailyViewsResponse get_you_tube_daily_views(video_id, account_id, from_date, to_date, start_date, end_date)
Get YouTube daily views

Returns daily view counts for a YouTube video including views, watch time, and subscriber changes. Requires yt-analytics.readonly scope (re-authorization may be needed).  - YouTube finalizes analytics with a ~3-day delay. By default only finalized days are returned; an explicit endDate can reach into the delay window (see the endDate parameter). - Max 90 days, defaults to last 30 days. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**video_id** | **String** | The YouTube video ID (e.g., \"dQw4w9WgXcQ\") | [required] |
**account_id** | **String** | The Zernio account ID for the YouTube account | [required] |
**from_date** | Option<**String**> | Start date (YYYY-MM-DD). Defaults to 30 days ago. |  |
**to_date** | Option<**String**> | End date (YYYY-MM-DD). Defaults to 3 days ago, the newest fully finalized day (YouTube finalizes analytics with a ~3-day delay).  An explicit toDate is honored up to today. Days inside the delay window are provisional and may still be revised by YouTube (see provisionalSince in the response); days YouTube has not processed yet are omitted from dailyViews.  |  |
**start_date** | Option<**String**> | Alias of fromDate, kept for existing callers |  |
**end_date** | Option<**String**> | Alias of toDate, kept for existing callers |  |

### Return type

[**models::YouTubeDailyViewsResponse**](YouTubeDailyViewsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_you_tube_demographics

> models::YouTubeDemographicsResponse get_you_tube_demographics(account_id, video_id, breakdown, from_date, to_date, start_date, end_date)
Get YouTube demographics

Returns audience demographic insights for a YouTube channel, broken down by age, gender, and/or country. Pass videoId to get the audience profile of a single video instead of the whole channel.  - Age and gender values are viewer percentages (0-100). - Country values are view counts.  Data is based on signed-in viewers only, with a 2-3 day delay. YouTube suppresses demographics for videos with too few signed-in views, so low-traffic videos can return empty breakdowns. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio SocialAccount ID for the YouTube account | [required] |
**video_id** | Option<**String**> | YouTube video ID. When provided, demographics are scoped to this single video (must belong to the connected channel; otherwise 404 video_not_found).  |  |
**breakdown** | Option<**String**> | Comma-separated list of demographic dimensions: age, gender, country. Defaults to all three if omitted.  |  |
**from_date** | Option<**String**> | Start date in YYYY-MM-DD format. Defaults to 90 days ago, or to the video's publish date (lifetime) when videoId is provided.  |  |
**to_date** | Option<**String**> | End date (YYYY-MM-DD). Defaults to 3 days ago, the newest fully finalized day (YouTube finalizes analytics with a ~3-day delay). An explicit toDate is honored up to today: days inside the delay window are provisional and may still be revised by YouTube (see provisionalSince in the response).  |  |
**start_date** | Option<**String**> | Alias of fromDate, kept for existing callers |  |
**end_date** | Option<**String**> | Alias of toDate, kept for existing callers |  |

### Return type

[**models::YouTubeDemographicsResponse**](YouTubeDemographicsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_you_tube_video_retention

> models::YouTubeVideoRetentionResponse get_you_tube_video_retention(video_id, account_id, from_date, to_date, start_date, end_date)
Get YouTube video retention curve

Returns the audience retention curve for a single YouTube video, plus the video's duration for rendering the curve on a time axis. Requires yt-analytics.readonly scope (re-authorization may be needed).  ### The curve  - Up to 100 points (elapsedVideoTimeRatio 0.01-1.0), aggregated over the whole date range. YouTube does not support per-day retention breakdowns. - audienceWatchRatio: the absolute share of viewers watching at that point in the video. It can exceed 1 (rewinds and looping, common on Shorts). - relativeRetentionPerformance: compares against videos of similar length (0 = worst, 0.5 = median, 1 = best).  ### Empty curves  YouTube returns an empty curve for videos with very few views or before analytics processing completes (2-3 day delay). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**video_id** | **String** | The YouTube video ID (e.g., \"dQw4w9WgXcQ\") | [required] |
**account_id** | **String** | The Zernio account ID for the YouTube account | [required] |
**from_date** | Option<**String**> | Start date (YYYY-MM-DD). Defaults to the video's publish date (lifetime curve). |  |
**to_date** | Option<**String**> | End date (YYYY-MM-DD). Defaults to 3 days ago, the newest fully finalized day (YouTube finalizes analytics with a ~3-day delay). An explicit toDate is honored up to today: days inside the delay window are provisional and may still be revised by YouTube (see provisionalSince in the response).  |  |
**start_date** | Option<**String**> | Alias of fromDate, kept for existing callers |  |
**end_date** | Option<**String**> | Alias of toDate, kept for existing callers |  |

### Return type

[**models::YouTubeVideoRetentionResponse**](YouTubeVideoRetentionResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_facebook_tagged_posts

> models::ListFacebookTaggedPosts200Response list_facebook_tagged_posts(account_id, limit, cursor)
List the posts a Facebook Page is tagged in

Returns the public posts where other people or Pages tagged the connected Facebook Page, as Meta returns them from the Page's `tagged` edge.  Cursor-paginated: pass `nextCursor` from the previous response as `cursor` to read the next page. `nextCursor` is null when there are no more pages. Meta does not say whether a page is the last one, so the final page can come back empty with `nextCursor` null.  Works for `facebook` accounts with a Page selected. Meta needs the `pages_read_user_content` permission on the connection: a connection made without it gets Meta's refusal back as `platform_api_error`, and reconnecting the account grants it. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The ID of a connected Facebook account. | [required] |
**limit** | Option<**i32**> | Page size. |  |[default to 25]
**cursor** | Option<**String**> | The `nextCursor` of the previous page. |  |

### Return type

[**models::ListFacebookTaggedPosts200Response**](listFacebookTaggedPosts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_facebook_visitor_posts

> models::ListFacebookVisitorPosts200Response list_facebook_visitor_posts(account_id, limit, cursor)
List visitor posts on a Facebook Page

Returns the posts other people published on the connected Facebook Page, newest first. A Page without visitor posts returns an empty `data` array.  ### What is returned  Zernio reads the Page feed (Graph `/{page-id}/feed`, which works on New Pages Experience Pages, unlike the deprecated `visitor_posts` edge). It drops:  - the posts the Page published itself - the posts other people published on their own timeline that only tag the Page  ### Pagination  Cursor-paginated: pass `nextCursor` from the previous response as `cursor` to read the next page.  `limit` sets how many feed entries are scanned, so a page can hold fewer posts than `limit`, or none, while `nextCursor` is not null. `nextCursor` is null when there are no more pages, and the final page can come back empty.  ### Requirements  Works on `facebook` accounts with a Page selected. Meta requires the `pages_read_user_content` permission, which Zernio requests with the comments scope. An account connected without it receives Meta's refusal as `platform_api_error`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The ID of a connected Facebook Page account. | [required] |
**limit** | Option<**i32**> | Number of Page feed entries to scan. The Page's own posts are dropped from them. |  |[default to 25]
**cursor** | Option<**String**> | The `nextCursor` of the previous page. |  |

### Return type

[**models::ListFacebookVisitorPosts200Response**](listFacebookVisitorPosts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_post_authenticity

> models::ListPostAuthenticity200Response list_post_authenticity(account_id, min_score, max_score, from, to, limit, skip)
List authenticity scores

Lists the stored authenticity scores for one connected account, newest first. Requires the Analytics add-on.  Scores are 0 to 100 and come from Zernio's own model over verified platform samples.  ### Filters  - `minScore` and `maxScore`: find posts that look inflated. - `from` and `to`: bound when the score was computed. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The connected account to list scores for. | [required] |
**min_score** | Option<**i32**> | Only scores at or above this value. |  |
**max_score** | Option<**i32**> | Only scores at or below this value. |  |
**from** | Option<**String**> | Only scores computed at or after this time (ISO 8601). |  |
**to** | Option<**String**> | Only scores computed at or before this time (ISO 8601). |  |
**limit** | Option<**i32**> | Page size. |  |[default to 50]
**skip** | Option<**i32**> | Number of scores to skip. |  |[default to 0]

### Return type

[**models::ListPostAuthenticity200Response**](listPostAuthenticity_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_tracking_windows

> models::ListTrackingWindows200Response list_tracking_windows(account_id, status, limit, skip)
List tracking windows

Lists the tracking windows you can see, newest first. Each window carries the latest verified numbers we read from the platform. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | Option<**String**> | Only windows for this connected account. |  |
**status** | Option<**String**> | Only windows in this status. |  |
**limit** | Option<**i32**> | Page size. |  |[default to 50]
**skip** | Option<**i32**> | Number of windows to skip. |  |[default to 0]

### Return type

[**models::ListTrackingWindows200Response**](listTrackingWindows_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## open_tracking_window

> models::TrackingWindowResponse open_tracking_window(open_tracking_window_request)
Open a tracking window

Starts watching a post's views and engagement.  Zernio fetches the numbers from the platform itself on its regular analytics sync, so every reading is verified. It is a value we read from the platform, never one the creator or the caller reported.  ### The window  - Runs for `trackingDays` (30 by default, 90 at most). - Ends with one final read, after which the `post.tracking_completed` webhook fires.  ### Identifying the post  Send either `postId` (an external post id from Zernio), or `accountId` together with the post's `url`.  ### Responses  - `201`: a new window was opened. - `200`: the post is already tracked; the existing window is returned. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**open_tracking_window_request** | [**OpenTrackingWindowRequest**](OpenTrackingWindowRequest.md) |  | [required] |

### Return type

[**models::TrackingWindowResponse**](TrackingWindowResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## run_google_analytics_realtime_report

> models::GoogleAnalyticsReport run_google_analytics_realtime_report(run_google_analytics_realtime_report_request)
Run a Google Analytics (GA4) realtime report

Activity on a connected GA4 property in the last 30 minutes (up to 60 for Analytics 360), through Google's `runRealtimeReport`. Not cached. Only realtime dimensions and metrics are accepted, e.g. `country`, `unifiedScreenName` with `activeUsers`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**run_google_analytics_realtime_report_request** | [**RunGoogleAnalyticsRealtimeReportRequest**](RunGoogleAnalyticsRealtimeReportRequest.md) |  | [required] |

### Return type

[**models::GoogleAnalyticsReport**](GoogleAnalyticsReport.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## run_google_analytics_report

> models::GoogleAnalyticsReport run_google_analytics_report(run_google_analytics_report_request)
Run a Google Analytics (GA4) report

Runs a report on a connected GA4 property through Google's Data API (`runReport`).  Pick any GA4 dimensions and metrics; filters and ordering use Google's own shapes.  ### Caching and quota  Identical requests on the same property are cached for 10 minutes.  Google meters each property by quota tokens. When it is used up the request returns 429 until Google refills it (hourly quotas within the hour, daily ones at midnight Pacific time). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**run_google_analytics_report_request** | [**RunGoogleAnalyticsReportRequest**](RunGoogleAnalyticsReportRequest.md) |  | [required] |

### Return type

[**models::GoogleAnalyticsReport**](GoogleAnalyticsReport.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## sync_external_posts

> models::SyncExternalPosts200Response sync_external_posts(sync_external_posts_request)
Sync an external post

Fetch an account's latest external posts (published directly on the platform, not through Zernio) on demand. A newly published post is then retrievable within seconds instead of waiting for the background sync, which refreshes each account at most every ~90 minutes.  Primary use case: verifying a submitted post. When a user publishes on the platform and immediately pastes the post URL into your app, call this with `accountId` plus `url` (or `postId`) to confirm the post exists and return its metadata.  ### Behavior  - Account access and connection state are checked before any platform call, including requests inside the debounce window. - Inactive accounts or accounts marked `needsReconnection` return `409` with code `ads_connection_required`. Stop scheduled retries for that account until it is reconnected, then read `GET /v1/accounts` for its current account ID. - For connected accounts, we fetch the latest posts live from the platform, then match and return the submitted post. - Requests are debounced per account (~15s): if the account was synced inside that window, the live fetch is skipped.  ### Account and platforms  `accountId` is required, because a post URL or id alone cannot be resolved to an account. The account must be connected to Zernio (we use its token to read the platform).  Supported for every platform with a listing API: Instagram, Facebook, TikTok, YouTube, X, Threads, Pinterest, Reddit, Bluesky, Google Business Profile, and LinkedIn organization accounts.  ### Locating the post  `url` accepts any format the platform uses, for example:  - `instagram.com/p/…`, `instagram.com/reel/…` - `youtu.be/…`, `youtube.com/shorts/…` - `tiktok.com/@user/video/…`, `vm.tiktok.com` short links - `pinterest.com/pin/…` on any regional domain, and `pin.it` short links  Pass `postId` (the platform media/video/pin id) as an alternative locator.  ### LinkedIn personal profiles  LinkedIn has no listing API for personal profiles, so a `url` is REQUIRED and imports that single post. Pass any LinkedIn post URL (`linkedin.com/posts/…`, `linkedin.com/feed/update/urn:li:activity:…`) or a `urn:li:share:…` / `urn:li:ugcPost:…` URN.  It works for posts published outside Zernio and before the account was connected, at any age. The post must be authored by the connected member.  Imported posts return full analytics (impressions, reach, reactions, comments, reshares, saves) and keep refreshing on the background analytics cycle. They carry no content/media, since LinkedIn does not expose them for personal profiles.  `publishedAt` comes from the post id:  - An activity URL (`linkedin.com/feed/update/urn:li:activity:…`) carries the publication time. - A `urn:li:share:…` / `urn:li:ugcPost:…` URN only carries the creation time, which is earlier for a post scheduled in another tool.  Pass the activity URL for the exact publication date. Importing it again for a post already imported by its URN corrects `publishedAt` on the same record.  Right after an import, the per-post `GET /v1/analytics?postId=` read can show zeros for a few minutes while the metrics are ingested. This endpoint's response carries the fetched values immediately.  ### TikTok Business accounts  A `postId` or TikTok `url` that the listing has not stored is fetched from TikTok and imported as an external post, at any age, with its current metrics.  ### Analytics delay  Post-level analytics (reach, impressions) still carry the platform's own delay (e.g. ~24h on Instagram). This endpoint confirms the post exists and returns its metadata plus basic engagement (likes, comments), not delayed insights. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sync_external_posts_request** | [**SyncExternalPostsRequest**](SyncExternalPostsRequest.md) |  | [required] |

### Return type

[**models::SyncExternalPosts200Response**](syncExternalPosts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

