# PostSample

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**synced_at** | **String** | When Zernio fetched this reading from the platform | 
**views** | **i32** |  | 
**likes** | **i32** |  | 
**comments** | **i32** |  | 
**shares** | Option<**i32**> | Null on platforms that do not return shares | 
**saves** | Option<**i32**> | Null on platforms that do not return saves | 
**watch_seconds** | Option<**f64**> | Average watch time in seconds. Null when the platform gives none. | 
**completion_rate** | Option<**f64**> | Share of viewers who watched to the end, 0 to 1. Null when the platform gives none. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


