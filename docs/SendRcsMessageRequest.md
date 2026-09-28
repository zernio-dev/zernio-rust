# SendRcsMessageRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**agent_id** | **String** |  | 
**to** | **String** | Recipient number (E.164; formatting is normalized). | 
**text** | Option<**String**> |  | [optional]
**content** | Option<[**models::RcsContent**](RcsContent.md)> |  | [optional]
**fallback_text** | Option<**String**> |  | [optional]
**ttl_seconds** | Option<**i32**> | Seconds before an undelivered message expires. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


