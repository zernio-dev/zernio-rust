# WebhookPayloadReactionReaction

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**emoji** | **String** | The emoji reacted with. May be an empty string when `action` is `removed` on WhatsApp (Meta does not report which emoji was removed).  | 
**action** | **Action** |  (enum: added, removed) | 
**message_id** | Option<**String**> | Internal Zernio message ID of the reacted-to message, when resolvable from the platform ID. | [optional]
**platform_message_id** | **String** | Platform-native ID of the reacted-to message (e.g. WhatsApp wamid). | 
**sender** | [**models::WebhookPayloadReactionReactionSender**](WebhookPayloadReactionReactionSender.md) |  | 
**reacted_at** | **String** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


