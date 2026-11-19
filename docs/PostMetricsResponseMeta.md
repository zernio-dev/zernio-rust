# PostMetricsResponseMeta

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**stale** | **bool** | True when the analytics backend was over capacity and part of this answer came from a stored copy instead of a live read. | 
**stale_since** | **String** | With stale=true: when the oldest stored copy used stopped being fresh. | 
**entity** | **Entity** |  (enum: posts) | 
**granularity** | **Granularity** |  (enum: total, day) | 
**from_date** | Option<**String**> |  | 
**to_date** | Option<**String**> |  | 
**missing_ids** | **Vec<String>** | Ids asked that match no published post the caller can read. | 
**total** | Option<**i32**> |  | 
**metrics_sample** | Option<[**models::PostMetricsResponseMetaAllOfMetricsSample**](PostMetricsResponseMetaAllOfMetricsSample.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


