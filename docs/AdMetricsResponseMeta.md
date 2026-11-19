# AdMetricsResponseMeta

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**stale** | **bool** | True when the analytics backend was over capacity and part of this answer came from a stored copy instead of a live read. | 
**stale_since** | **String** | With stale=true: when the oldest stored copy used stopped being fresh. | 
**from_date** | Option<**String**> |  | 
**to_date** | Option<**String**> |  | 
**backfill_pending** | **bool** | True while older metrics for the window are still being fetched from the platform. | 
**missing_ids** | **Vec<String>** | Asked ids that are not ads the caller can see. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


