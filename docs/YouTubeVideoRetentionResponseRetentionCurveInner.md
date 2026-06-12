# YouTubeVideoRetentionResponseRetentionCurveInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**elapsed_video_time_ratio** | Option<**f64**> | Position in the video as a ratio (0.01-1.0, exclusive end of each interval) | [optional]
**audience_watch_ratio** | Option<**f64**> | Absolute share of viewers watching at this point. Can exceed 1 (rewinds/looping, common on Shorts). | [optional]
**relative_retention_performance** | Option<**f64**> | Retention vs videos of similar length (0 = worst, 0.5 = median, 1 = best) | [optional]
**started_watching** | Option<**i32**> | Viewers who started watching in this segment | [optional]
**stopped_watching** | Option<**i32**> | Viewers who stopped watching in this segment | [optional]
**total_segment_impressions** | Option<**i32**> | Total views of this segment, including rewatches | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


