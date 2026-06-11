# SendInboxMessageRequestTemplateElementsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | Option<**String**> | Element title (max 80 chars). Required for Instagram/Facebook generic templates. | [optional]
**subtitle** | Option<**String**> | Element subtitle (Instagram/Facebook only) | [optional]
**image_url** | Option<**String**> | Element image URL (Instagram/Facebook only) | [optional]
**buttons** | Option<[**Vec<models::SendInboxMessageRequestTemplateElementsInnerButtonsInner>**](SendInboxMessageRequestTemplateElementsInnerButtonsInner.md)> | Element buttons (Instagram/Facebook only) | [optional]
**name** | Option<**String**> | WhatsApp only. Name of the approved template to send. | [optional]
**language** | Option<**String**> | WhatsApp only. Template language code (e.g. en_US). | [optional]
**components** | Option<**Vec<std::collections::HashMap<String, serde_json::Value>>**> | WhatsApp only. Meta Cloud API send-shape components array, forwarded to Meta verbatim. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


