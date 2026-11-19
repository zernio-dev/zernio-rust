# PostMetricSample

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**synced_at** | **String** | When Zernio read the numbers from the platform. | 
**views** | **f64** |  | 
**likes** | **f64** |  | 
**comments** | **f64** |  | 
**shares** | Option<**f64**> | null on platforms that do not return the counter, unlike a real 0. | 
**saves** | Option<**f64**> | null on platforms that do not return the counter, unlike a real 0. | 
**watch_seconds** | Option<**f64**> | Average watch time; null when the platform gives no watch signal. | 
**completion_rate** | Option<**f64**> | null when the platform gives no watch signal. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


