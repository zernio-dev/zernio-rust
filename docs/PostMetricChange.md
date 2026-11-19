# PostMetricChange

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** |  | 
**profile_id** | **String** |  | 
**platform** | **String** |  | 
**platform_post_id** | **String** |  | 
**published_at** | **String** |  | 
**synced_at** | **String** | When the account's sync cycle that read these numbers started. Not an order: resume with the cursor only. | 
**deleted** | **bool** | True when the post was removed from the platform. | 
**metrics** | **std::collections::HashMap<String, f64>** | Each metric asked, as the platform reported it in this change; null when the post's platform does not report it. | 
**breakdowns** | Option<[**std::collections::HashMap<String, models::PostMetricRowBreakdownsValue>**](PostMetricRowBreakdownsValue.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


