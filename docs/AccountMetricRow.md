# AccountMetricRow

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**date** | **String** | Start of the period: the day, the Monday of the week or the first of the month, never before fromDate. With granularity=total, fromDate. | 
**account_id** | Option<**String**> | With groupBy=account. | 
**platform** | Option<**String**> | With groupBy=account or groupBy=platform. | 
**profile_id** | Option<**String**> | With groupBy=account. | 
**username** | Option<**String**> | With groupBy=account. | 
**metrics** | **std::collections::HashMap<String, f64>** | Each metric asked; null when no account in the row reports it or no follower snapshot exists in the period. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


