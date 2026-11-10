# WebhookPayloadPostPost

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**content** | Option<**String**> | Absent once publishing finishes when the team does not retain content. | [optional]
**content_not_retained** | Option<**bool**> | True when this team does not retain content and the post text was already cleared. | [optional]
**status** | **String** |  | 
**scheduled_for** | **String** |  | 
**published_at** | Option<**String**> |  | [optional]
**platforms** | [**Vec<models::WebhookPayloadPostPostPlatformsInner>**](WebhookPayloadPostPostPlatformsInner.md) |  | 
**metadata** | Option<**std::collections::HashMap<String, serde_json::Value>**> | The free-form `metadata` object supplied when the post was created, echoed back so you can map events onto your own records. Omitted when the post was created without it. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


