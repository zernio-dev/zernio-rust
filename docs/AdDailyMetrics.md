# AdDailyMetrics

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**spend** | Option<**f64**> |  | [optional]
**impressions** | Option<**i32**> |  | [optional]
**reach** | Option<**i32**> |  | [optional]
**clicks** | Option<**i32**> |  | [optional]
**ctr** | Option<**f64**> | Click-through rate (%) | [optional]
**cpc** | Option<**f64**> | Cost per click | [optional]
**cpm** | Option<**f64**> | Cost per 1000 impressions | [optional]
**engagement** | Option<**i32**> |  | [optional]
**conversions** | Option<**i32**> | Count of conversion events over the requested date range. Meta: events matching the campaign's promoted_object.custom_event_type (PURCHASE, LEAD, etc.). Google: the account's tracked conversions. X and LinkedIn: their reported website/lead conversions (added 2026-07). 0 for non-conversion campaigns or when no events have fired. | [optional]
**cost_per_conversion** | Option<**f64**> | Derived spend / conversions in the same currency as spend. 0 when conversions is 0. | [optional]
**actions** | Option<**std::collections::HashMap<String, i32>**> | Per-action-type counts summed over the date range, keyed by the platform's action-type names. Meta: raw Insights action_type keys (link_click, offsite_conversion.fb_pixel_purchase, onsite_conversion.lead_grouped, ...) — both engagement and conversion events. X: conversion types (purchase, sign_up, site_visit, download, custom). LinkedIn: conversion types (post_click, post_view, lead_gen). Google returns {} (its per-action names aren't synced per ad). Empty object when no actions are reported. NOTE: keys differ by platform, so branch on the ad's platform when interpreting them. | [optional]
**action_values** | Option<**std::collections::HashMap<String, f64>**> | Monetary mirror of `actions`, from Meta's Insights `action_values[]` array. Same keying — values are the revenue attributed to each action_type, in ad-account native currency (same unit as `spend`; see the campaign node's `currency` field). Use this to compute revenue-per-event (e.g. avg purchase value). Meta-only; other platforms return {}. | [optional]
**purchase_value** | Option<**f64**> | Convenience sum of purchase-type action values — picked from `actionValues` via the same priority list as `conversions` so both fields describe the same events. In ad-account native currency. 0 when the campaign has no purchase event configured. Meta-only. | [optional]
**roas** | Option<**f64**> | Return on ad spend — derived as `purchaseValue / spend`. 0 when `spend` is 0. Equivalent to Meta's `purchase_roas` under default attribution. At ad-set and campaign levels this is recomputed from summed purchaseValue + spend (NOT averaged across children) so it's mathematically correct at every rollup level. | [optional]
**video_play_actions** | Option<**i32**> | Meta video ads only (0 for non-video ads and other platforms), like all video* fields below. Number of times the video started playing (Meta `video_play_actions`), summed over the date range and across children at ad-set/campaign level. | [optional]
**video30_sec_watched_actions** | Option<**i32**> | Views of at least 30 seconds (or to the end, for shorter videos). Meta `video_30_sec_watched_actions`. | [optional]
**video_thruplay_watched_actions** | Option<**i32**> | ThruPlays (watched to completion, or at least 15 seconds). Meta `video_thruplay_watched_actions`. | [optional]
**video_p25_watched_actions** | Option<**i32**> | Views reaching 25% of the video's length. With the other percentile fields, powers hook/hold/drop-off analysis (e.g. hook rate = videoP25WatchedActions / videoPlayActions). Meta `video_p25_watched_actions`. | [optional]
**video_p50_watched_actions** | Option<**i32**> | Views reaching 50% of the video's length. Meta `video_p50_watched_actions`. | [optional]
**video_p75_watched_actions** | Option<**i32**> | Views reaching 75% of the video's length. Meta `video_p75_watched_actions`. | [optional]
**video_p95_watched_actions** | Option<**i32**> | Views reaching 95% of the video's length. Meta `video_p95_watched_actions`. | [optional]
**video_p100_watched_actions** | Option<**i32**> | Views reaching 100% of the video's length. Meta `video_p100_watched_actions`. | [optional]
**video_avg_time_watched_actions** | Option<**f64**> | Average seconds watched per play (Meta `video_avg_time_watched_actions`). Aggregated over date ranges and across children as a play-weighted average (total watch time / total plays), never a plain average of averages. | [optional]
**last_synced_at** | Option<**String**> | Present on individual ads only, not on campaign aggregations | [optional]
**date** | Option<[**String**](String.md)> | Calendar day (YYYY-MM-DD) these metrics apply to. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


