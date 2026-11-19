# AccountMetricsResponseMeta

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**stale** | **bool** | True when the analytics backend was over capacity and part of this answer came from a stored copy instead of a live read. | 
**stale_since** | **String** | With stale=true: when the oldest stored copy used stopped being fresh. | 
**entity** | **Entity** |  (enum: accounts) | 
**granularity** | **Granularity** |  (enum: total, day, week, month) | 
**group_by** | **GroupBy** |  (enum: account, platform, none) | 
**attribution** | **Attribution** |  (enum: publish, received) | 
**from_date** | **String** |  | 
**to_date** | **String** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


