# WhatsAppConversationalAutomation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enable_welcome_message** | Option<**bool**> | When true, Meta sends a `request_welcome` event the first time a person opens a chat with the number. | [optional]
**prompts** | Option<**Vec<String>**> | Ice breakers shown to a person opening a chat. Tapping one sends its text as a normal message. | [optional]
**commands** | Option<[**Vec<models::WhatsAppConversationalAutomationCommandsInner>**](WhatsAppConversationalAutomationCommandsInner.md)> | Slash commands shown when a person types `/`. Names are unique, letters, digits and underscores, without the slash. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


