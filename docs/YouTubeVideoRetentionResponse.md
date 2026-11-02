# YouTubeVideoRetentionResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | Option<**bool**> |  | [optional]
**account_id** | Option<**String**> | The Zernio account ID for the YouTube account | [optional]
**video_id** | Option<**String**> | The YouTube video ID | [optional]
**title** | Option<**String**> | Video title | [optional]
**published_at** | Option<**String**> | When the video was published on YouTube | [optional]
**duration_seconds** | Option<**i32**> | Video length in seconds (from YouTube contentDetails.duration) | [optional]
**date_range** | Option<[**models::YouTubeDailyViewsResponseDateRange**](YouTubeDailyViewsResponseDateRange.md)> |  | [optional]
**provisional_since** | Option<[**String**](String.md)> | Present only when the range reaches into YouTube's ~3-day processing window: the first date whose numbers are provisional and may still be revised by YouTube. | [optional]
**segment_metrics_available** | Option<**bool**> | Whether YouTube returned startedWatching and stoppedWatching for this curve. When false, both are 0 placeholders in every point, not measured values. | [optional]
**retention_curve** | Option<[**Vec<models::YouTubeVideoRetentionResponseRetentionCurveInner>**](YouTubeVideoRetentionResponseRetentionCurveInner.md)> | Up to 100 points covering the video timeline, aggregated over the date range. Contains only the buckets YouTube reports for that range and is never zero-filled, so it can end before 1.0, skip positions, or be empty. | [optional]
**note** | Option<**String**> | Present only when the curve is empty, explaining why | [optional]
**scope_status** | Option<[**models::YouTubeDailyViewsResponseScopeStatus**](YouTubeDailyViewsResponseScopeStatus.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


