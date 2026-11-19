# AdMetricRow

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ad_id** | **String** |  | 
**name** | **String** |  | 
**platform** | **String** |  | 
**status** | **String** |  | 
**currency** | Option<**String**> |  | 
**summary** | [**models::AdMetricRowSummary**](AdMetricRowSummary.md) |  | 
**daily** | Option<[**Vec<models::AdMetricRowDailyInner>**](AdMetricRowDailyInner.md)> | With granularity=day: one point per day. | [optional]
**breakdowns** | Option<**std::collections::HashMap<String, serde_json::Value>**> | With breakdowns: read live from the platform. | [optional]
**unsupported_breakdowns** | Option<**Vec<String>**> |  | [optional]
**breakdown_hints** | Option<**std::collections::HashMap<String, String>**> |  | [optional]
**breakdowns_range** | Option<**serde_json::Value**> |  | [optional]
**breakdown_errors** | Option<**Vec<serde_json::Value>**> |  | [optional]
**breakdown_dropped_metrics** | Option<[**std::collections::HashMap<String, Vec<String>>**](Vec.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


