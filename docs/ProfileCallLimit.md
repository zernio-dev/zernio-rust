# ProfileCallLimit

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**limit** | Option<**f64**> | The limit, or null when none is set at this level. | 
**used** | **f64** | Used in the current window, calls still in progress included. | 
**remaining** | Option<**f64**> | What is left before the limit; null when there is no limit. | 
**window** | **Window** | `concurrent` counts calls in progress now; the rolling windows end now. (enum: concurrent, rolling_hour, rolling_24h) | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


