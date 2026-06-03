# UpdatePostRequestPlatformsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **String** |  | 
**account_id** | **String** |  | 
**custom_content** | Option<**String**> | Platform-specific text override. | [optional]
**custom_media** | Option<[**Vec<models::MediaItem>**](MediaItem.md)> |  | [optional]
**scheduled_for** | Option<**String**> | Optional per-platform scheduled time override. | [optional]
**platform_specific_data** | Option<**std::collections::HashMap<String, serde_json::Value>**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


