# WebhookPayloadPostPlatformPost

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**content** | **String** |  | 
**status** | **String** | Post-level status AT FIRE TIME. May still be `publishing` if other platforms haven't terminated; check this field rather than assuming.  | 
**scheduled_for** | **String** |  | 
**published_at** | Option<**String**> |  | [optional]
**platforms** | [**Vec<models::WebhookPayloadPostPlatformPostPlatformsInner>**](WebhookPayloadPostPlatformPostPlatformsInner.md) |  | 
**metadata** | Option<**std::collections::HashMap<String, serde_json::Value>**> | The free-form `metadata` object supplied when the post was created, echoed back so you can map events onto your own records. Omitted when the post was created without it. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


