# \MetricsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_account_metrics**](MetricsApi.md#get_account_metrics) | **GET** /v1/metrics/accounts | Read follower and post totals per account, platform or scope over time
[**get_ad_account_metrics**](MetricsApi.md#get_ad_account_metrics) | **GET** /v1/metrics/ad-accounts | Read the uploaded results summed across ad accounts
[**get_ad_metrics**](MetricsApi.md#get_ad_metrics) | **GET** /v1/metrics/ads | Read ad metrics by id, or one ad day by day with breakdowns
[**get_campaign_metrics**](MetricsApi.md#get_campaign_metrics) | **GET** /v1/metrics/campaigns | Read the uploaded results of each campaign over a window
[**get_inbox_metrics**](MetricsApi.md#get_inbox_metrics) | **GET** /v1/metrics/inbox | Read message volume and response times
[**get_insight_metrics**](MetricsApi.md#get_insight_metrics) | **GET** /v1/metrics/insights | Read live account or post insights from the platform
[**get_metrics_catalog**](MetricsApi.md#get_metrics_catalog) | **GET** /v1/metrics/catalog | List the metrics, groupings and limits of each metrics endpoint
[**get_post_metrics**](MetricsApi.md#get_post_metrics) | **GET** /v1/metrics/posts | Read post metrics by id, day by day, as a list, or grouped



## get_account_metrics

> models::AccountMetricsResponse get_account_metrics(account_id, profile_id, metrics, group_by, from_date, to_date, platform, granularity, attribution, limit, cursor)
Read follower and post totals per account, platform or scope over time

Reads followers, the account counters the platform reports (media count, video count...) and the totals of the posts each account published, per account, per platform or for the whole scope, for the whole window or by day, week or month.  - Scope: exactly one of `accountId` (up to 25) or `profileId` (one, with an optional `platform`). - `groupBy`: `account` (the default, one row per account and period), `platform` or `none`. - `granularity`: `total` (the default), `day`, `week` (rows start on Monday) or `month`. A row's `date` is the start of its period, never before `fromDate`. - `attribution`: `publish` (the default) counts each post on the day it was published; `received` counts each interaction on the day it arrived, for windows up to 92 days. - `granularity=week&groupBy=platform&metrics=postCount,engagementRate`: how many posts each platform got per week and their pooled engagement rate. The newer way to read `GET /v1/analytics/posting-frequency`.  Without `fromDate` and `toDate` it reads the last 90 days; the window is at most 366 days. Followers are one value per day, taken at 02:00 UTC. `GET /v1/metrics/catalog?entity=accounts` lists every metric with the platforms that report it.  Each team has an analytics compute budget of 24 seconds per 30-second window across these reads: a request that would pass it is refused with 429 `details.scope: team_budget` before it runs.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | Option<**String**> | Comma-separated account ids, up to 25. |  |
**profile_id** | Option<**String**> | One profile id. |  |
**metrics** | Option<**String**> | Comma-separated metric names from the catalog. Defaults to every metric. |  |
**group_by** | Option<**String**> | Comma-separated groupings from the catalog, at most 2. |  |
**from_date** | Option<**String**> | First day, inclusive (YYYY-MM-DD, UTC). |  |
**to_date** | Option<**String**> | Last day, inclusive (YYYY-MM-DD, UTC). |  |
**platform** | Option<**String**> | Only with profileId. |  |
**granularity** | Option<**String**> |  |  |[default to total]
**attribution** | Option<**String**> |  |  |[default to publish]
**limit** | Option<**i32**> | Rows per page, 50 by default, 100 at most. |  |[default to 50]
**cursor** | Option<**String**> | pagination.nextCursor of the previous page, sent with the same query. |  |

### Return type

[**models::AccountMetricsResponse**](AccountMetricsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad_account_metrics

> models::AdAccountMetricsResponse get_ad_account_metrics(from_date, to_date, ad_account_id)
Read the uploaded results summed across ad accounts

Sums each result metric you uploaded across ad accounts (every ad account the key can read, or the platform ids in `adAccountId`) over `fromDate` to `toDate` (both required, at most 400 days), with the same metrics as `GET /v1/metrics/campaigns`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**from_date** | **String** | First day, inclusive. | [required] |
**to_date** | **String** | Last day, inclusive. The range is at most 400 days. | [required] |
**ad_account_id** | Option<**String**> | Comma-separated platform ad account ids. Defaults to every ad account the key sees. |  |

### Return type

[**models::AdAccountMetricsResponse**](AdAccountMetricsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad_metrics

> models::AdMetricsResponse get_ad_metrics(ad_id, granularity, from_date, to_date, breakdowns, attribution_windows)
Read ad metrics by id, or one ad day by day with breakdowns

Reads the delivery and conversion metrics Zernio synced from the ad networks for up to 100 Zernio ad ids (`adId`, as `GET /v1/ads` returns them). Ids you cannot read come back in `meta.missingIds`.  - `granularity=day` with one ad: one point per day. - `breakdowns` with one ad: read live from the network (age, gender, country, placement...), with `attributionWindows` for Meta.  Without `fromDate` and `toDate` it reads the last 90 days; the window is at most 730 days. `meta.backfillPending` is true while older days are still being fetched. Money is in the ad account currency (`currency`). `GET /v1/metrics/catalog?entity=ads` lists every metric with the networks that report it.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_id** | **String** | Comma-separated Zernio ad ids, up to 100. | [required] |
**granularity** | Option<**String**> | day reads one ad, one point per day. |  |[default to total]
**from_date** | Option<**String**> | Without fromDate and toDate, the last 90 days. |  |
**to_date** | Option<**String**> | Last day, inclusive (YYYY-MM-DD, UTC). |  |
**breakdowns** | Option<**String**> | Comma-separated breakdowns, read live from the platform. One ad only. |  |
**attribution_windows** | Option<**String**> | Meta attribution windows for the breakdowns, comma-separated. |  |

### Return type

[**models::AdMetricsResponse**](AdMetricsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_campaign_metrics

> models::CampaignMetricsResponse get_campaign_metrics(from_date, to_date, limit, cursor, campaign_id)
Read the uploaded results of each campaign over a window

Sums, per campaign, each result metric you uploaded (one key per metric, as `GET /v1/ads/campaign-results/metrics` lists them), with `cac_percent`, `cost_per_sale`, `cost_per_qualified_lead`, `lead_to_sale` and `qualified_rate` next to them, over `fromDate` to `toDate` (both required, at most 400 days).  Filter with `campaignId` (platform campaign ids); pages with `cursor`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**from_date** | **String** | First day, inclusive. | [required] |
**to_date** | **String** | Last day, inclusive. The range is at most 400 days. | [required] |
**limit** | Option<**i32**> | Rows per page, 50 by default, 100 at most. |  |[default to 50]
**cursor** | Option<**String**> | pagination.nextCursor of the previous page, sent with the same query. |  |
**campaign_id** | Option<**String**> | Comma-separated platform campaign ids. |  |

### Return type

[**models::CampaignMetricsResponse**](CampaignMetricsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_inbox_metrics

> models::InboxMetricsResponse get_inbox_metrics(conversation_id, account_id, profile_id, metrics, group_by, from_date, to_date, platform, source, granularity, sort, include, limit, cursor)
Read message volume and response times

Counts messages received, sent, read and failed, conversations and replies, and response times (median, p90, p99, mean, min, max) across the inbox, from the messages Zernio logged.  - Scope: `conversationId` (up to 25, one row per conversation), `accountId` (up to 25) or one `profileId`. Without a scope, every account the key can read. - `groupBy` (at most 2): `account`, `platform`, `source`, `hourOfWeek` (one row per UTC weekday and hour), `responseTimeBucket` (with `metrics=replied`) or `conversation` (paged with `cursor`, `include=total` counts up to 100,000). - `granularity`: `total` (the default), `day` or `week`. - `include=account` adds usernames to account rows; `include=conversation` adds the participant and last message to conversation rows.  Response time metrics are returned only when named in `metrics`. Without `fromDate` and `toDate` it reads the last 30 days; the window is at most 90 days. `GET /v1/metrics/catalog?entity=inbox` lists every metric, sort and groupBy.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | Option<**String**> | Comma-separated conversation ids (Zernio or platform), up to 25: one row per conversation. |  |
**account_id** | Option<**String**> | Comma-separated account ids, up to 25. |  |
**profile_id** | Option<**String**> | One profile id. |  |
**metrics** | Option<**String**> | Comma-separated metric names from the catalog. Defaults to the counts; response times only when named. |  |
**group_by** | Option<**String**> | Comma-separated groupings from the catalog, at most 2: account, conversation, platform, source, hourOfWeek, responseTimeBucket. |  |
**from_date** | Option<**String**> | First day, inclusive (YYYY-MM-DD, UTC). Defaults to 30 days before toDate. The window is at most 90 days. |  |
**to_date** | Option<**String**> | Last day, inclusive (YYYY-MM-DD, UTC). Defaults to today. |  |
**platform** | Option<**String**> | A messaging platform, such as instagram or whatsapp. |  |
**source** | Option<**String**> | Only messages sent from this source, such as api or broadcast. Not with response time metrics. |  |
**granularity** | Option<**String**> |  |  |[default to total]
**sort** | Option<**String**> | A sort from the catalog, such as messages-desc. With granularity=total. |  |
**include** | Option<**String**> | Comma-separated includes from the catalog: account, conversation, total. |  |
**limit** | Option<**i32**> | Rows returned with groupBy=account (10 by default, 100 at most) or groupBy=conversation (50 by default, 1,000 at most). |  |
**cursor** | Option<**String**> | With groupBy=conversation: pagination.nextCursor of the previous page. |  |

### Return type

[**models::InboxMetricsResponse**](InboxMetricsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_insight_metrics

> models::InsightMetricsResponse get_insight_metrics(account_id, metrics, platform_post_id, granularity, group_by, breakdown, timeframe, cursor, limit, include, from_date, to_date)
Read live account or post insights from the platform

Reads insights the platform computes and Zernio does not store (page views, profile visits, watch time, audience demographics...), live from the platform, for one account or one of its posts (`platformPostId`).  Platforms: Facebook, Instagram, LinkedIn, TikTok, YouTube, Pinterest, Google Business and Google Search Console. Another platform answers 400 on `accountId`, a disconnected account 401 `account_disconnected`, and a platform error the platform's own code under `platformError`.  - `granularity`: `total` (the default) or `day`. - `groupBy=demographic` with one metric and `breakdown` (age, gender, country, city...): one row per audience segment. LinkedIn: organizations only. - `groupBy=hour`: Instagram followers online per day and hour of the last 30 days. - `groupBy=keyword`: Google Business search keywords, one row per keyword, paged with `cursor`.  Google Search Console answers clicks, impressions, ctr (0 to 1) and position (1 is the top), final days only:  - Without groupBy: the site totals. `granularity=day` adds the date. - `groupBy` combines any of `query`, `page`, `country` and `device` (`groupBy=query,country`): one row per combination, most clicks first, with each value in `dimensions`. - Pages with `limit` (up to 25,000, 1,000 by default) and `cursor`. - `include=retentionCurve` with a YouTube `platformPostId`: the audience retention curve.  Without `fromDate` and `toDate` it reads the last 30 days; the window is at most 541 days. `GET /v1/metrics/catalog?entity=insights&platform=...` lists each platform's metrics. Metrics the platform cannot answer for this account are listed in `meta.unavailableMetrics` instead of failing the request.  Each request calls the platform: read each account every few minutes at most. These reads share the `account-insights` cap and the 120 reads per hour of one account.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | One account id. | [required] |
**metrics** | Option<**String**> | Comma-separated metric names (up to 25). Defaults to the platform's default metrics. `GET /v1/metrics/catalog?entity=insights&platform=...` lists them. |  |
**platform_post_id** | Option<**String**> | One post of the account, by its platform id: answers the post's live insights instead of the account's. |  |
**granularity** | Option<**String**> | Defaults to total; groupBy=hour answers per day. |  |
**group_by** | Option<**String**> | demographic: audience segments (age, gender, country...). hour: Instagram followers online per day and hour, last 30 days. keyword: Google Business search keywords per month. query, page, country, device: Google Search Console, combined with commas (groupBy=query,country). |  |
**breakdown** | Option<**String**> | With groupBy=demographic: comma-separated segments. Defaults to the platform's default segments. |  |
**timeframe** | Option<**String**> | Instagram demographics only. Defaults to this_month. |  |
**cursor** | Option<**String**> | With groupBy=keyword or a Search Console account: pagination.nextCursor of the previous page, sent with the same query. |  |
**limit** | Option<**i32**> | Search Console accounts only: rows per page. Defaults to 1,000. |  |
**include** | Option<**String**> | With platformPostId on YouTube: retentionCurve adds the audience retention curve. |  |
**from_date** | Option<**String**> | First day, inclusive (YYYY-MM-DD, UTC). Defaults to 30 days before toDate. The window is at most 541 days. |  |
**to_date** | Option<**String**> | Last day, inclusive (YYYY-MM-DD, UTC). Defaults to today. |  |

### Return type

[**models::InsightMetricsResponse**](InsightMetricsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_metrics_catalog

> models::MetricsCatalogResponse get_metrics_catalog(entity, platform)
List the metrics, groupings and limits of each metrics endpoint

Describes each metrics endpoint (`GET /v1/metrics/posts`, `/accounts`, `/insights`, `/inbox`, `/ads`, `/campaigns` and `/ad-accounts`): the scope it needs, the most ids per scope, the longest and default date window, the granularities, sorts, includes, groupBy values, attributions and every metric with its unit, platforms and freshness.  Read it once and cache it: it changes only when Zernio adds a metric or a grouping. Filter with `entity` and `platform` to get only what one screen needs. No analytics add-on is needed to read it.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**entity** | Option<**String**> | Only this entity. |  |
**platform** | Option<**String**> | Only the metrics, sorts, includes and groupBy values this platform has. Every entity is still listed. |  |

### Return type

[**models::MetricsCatalogResponse**](MetricsCatalogResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_post_metrics

> models::PostMetricsResponse get_post_metrics(post_id, platform_post_id, account_id, profile_id, metrics, group_by, from_date, to_date, platform, granularity, origin, sort, include, changed_since, limit, cursor)
Read post metrics by id, day by day, as a list, or grouped

Reads the metrics Zernio synced for published posts, Zernio posts and posts published outside Zernio alike. Send exactly one scope: `postId`, `platformPostId`, `accountId` or `profileId`, or read the change feed with `changedSince`.  - **By id** (`postId` or `platformPostId`, up to 100): one row per publication. Ids that match no post you can read come back in `meta.missingIds`. - **One post day by day**: one id with `granularity=day`. - **A list** (`accountId` up to 25, or one `profileId` with an optional `platform`): posts published in the window, newest first, paged with `cursor`. `sort` orders it by a metric (`likes-desc`, `engagement-desc`...), up to the 1,000 best posts. `include=total` counts the list on the first page (windows up to 92 days).  Grouped with `groupBy`:  - `post`: sums the platforms each post id was published to into one row (by id, `granularity=total`). - `dayOfWeek,hour`: one row per UTC weekday and hour the posts were published, summing each post's latest metrics. The newer way to read `GET /v1/analytics/best-time`. - `postAge`: the share of its final engagement a post had reached at each age (0-6h to 30d+), `engagementShareOfFinal`. The newer way to read `GET /v1/analytics/content-decay`. Defaults to the last 60 days. - `format`: one row per format (image, video, carousel, text). The newer way to read `GET /v1/analytics/format-breakdown`.  `dayOfWeek,hour`, `postAge` and `format` take a list scope (`accountId` or `profileId`), `granularity=total`, windows up to 92 days, and answer in one page.  Includes on rows read by id or in a list (`include`, comma-separated):  - `post`: content, media and publishing details. - `samples`: one reading per analytics sync, oldest first, the newest 500 per post, narrowed by `fromDate` and `toDate` on the sync time. Posts read by `postId` or `platformPostId` only, up to 10, with `granularity=total` and no `groupBy`. The newer way to read `GET /v1/analytics/samples`. - `authenticity`: the stored authenticity score with its confidence, reasons, model version, sample count and when it was computed; null until the post has been scored. The `authenticityScore` metric carries the score alone (0 to 100). - `impressionSources`, `audienceTypes`, `audienceCountries`, `retentionCurve`: breakdowns on the platforms that report them.  Change feed with `changedSince`:  - `changedSince=now` answers no rows and a starting cursor; send each `pagination.nextCursor` back as `changedSince` to get one `PostMetricChange` row per post whose metrics changed since then, oldest change first. - It reads every account the key can read, narrowed with one `profileId` and `platform`. It takes `metrics` from the feed's list and the breakdown includes, nothing else. - Changes are kept 7 days and a cursor older than 6 days is refused. The feed and its cursors are the same as `GET /v1/analytics/delta`, of which it is the newer way to read.  Without `fromDate` and `toDate` a list reads the last 90 days; the window is at most 366 days. `GET /v1/metrics/catalog?entity=posts` lists every metric, sort, include and groupBy, with the platforms that report each. A metric is `null` when the platform does not report it or the post has no snapshot yet.  Each team has an analytics compute budget of 24 seconds per 30-second window across these reads, on top of the per-group cap: a request that would pass it is refused with 429 `details.scope: team_budget` before it runs.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | Option<**String**> | Comma-separated post ids (Zernio or external), up to 100. |  |
**platform_post_id** | Option<**String**> | Comma-separated ids the platform gave the posts (a TikTok video id, a tweet id), up to 100. |  |
**account_id** | Option<**String**> | Comma-separated account ids, up to 25. |  |
**profile_id** | Option<**String**> | One profile id. |  |
**metrics** | Option<**String**> | Comma-separated metric names from the catalog. Defaults to every metric. |  |
**group_by** | Option<**String**> | Comma-separated groupings from the catalog, at most 2. |  |
**from_date** | Option<**String**> | First day, inclusive (YYYY-MM-DD, UTC). |  |
**to_date** | Option<**String**> | Last day, inclusive (YYYY-MM-DD, UTC). |  |
**platform** | Option<**String**> | Only with profileId. |  |
**granularity** | Option<**String**> | day reads one post. |  |[default to total]
**origin** | Option<**String**> | Lists only. Defaults to all. |  |
**sort** | Option<**String**> | A sort from the catalog, such as published-desc or likes-desc. |  |
**include** | Option<**String**> | Comma-separated includes from the catalog. |  |
**changed_since** | Option<**String**> | now (no rows, the starting cursor) or the previous pagination.nextCursor: one row per post whose metrics changed since, oldest first, across every account the key reads. Narrow with profileId and platform. Changes are kept 7 days; cursors older than 6 days are refused. |  |
**limit** | Option<**i32**> | Rows per page, 50 by default, 100 at most. |  |[default to 50]
**cursor** | Option<**String**> | pagination.nextCursor of the previous page, sent with the same query. |  |

### Return type

[**models::PostMetricsResponse**](PostMetricsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

