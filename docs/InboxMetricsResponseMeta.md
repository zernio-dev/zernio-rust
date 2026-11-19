# InboxMetricsResponseMeta

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**stale** | **bool** | True when the analytics backend was over capacity and part of this answer came from a stored copy instead of a live read. | 
**stale_since** | **String** | With stale=true: when the oldest stored copy used stopped being fresh. | 
**entity** | **Entity** |  (enum: inbox) | 
**granularity** | **Granularity** |  (enum: total, day, week) | 
**group_by** | **Vec<String>** |  | 
**from_date** | **String** |  | 
**to_date** | **String** |  | 
**total** | Option<**i32**> | With groupBy=conversation and include=total: the conversations the list holds, up to 100,000. | 
**total_is_capped** | **bool** | true when the conversation list holds more than 100,000 conversations. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


