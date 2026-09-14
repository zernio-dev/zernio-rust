# WebhookPayloadMessageDeliveryStatusError

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | Option<**i32**> |  | [optional]
**title** | Option<**String**> |  | [optional]
**message** | Option<**String**> |  | [optional]
**details** | Option<**String**> | Platform's extended detail for `code` (WhatsApp: Meta's `error_data.details`), when the platform sent one. Absent on SMS. | [optional]
**href** | Option<**String**> | Link to the platform's documentation for `code`, when the platform sent one. | [optional]
**explanation** | Option<**String**> | Plain-language translation of `code` (e.g. for 131026, that the recipient has likely opted out of marketing messages while utility templates are unaffected, or for 131031, that Meta restricted the WhatsApp Business Account). Null for unmapped codes; fall back to title/message.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


