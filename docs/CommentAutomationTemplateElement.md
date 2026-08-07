# CommentAutomationTemplateElement

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **String** | Card headline (80 chars max). Also used as the Inbox preview for the sent DM. | 
**subtitle** | Option<**String**> | Card description, e.g. the price or a short pitch (80 chars max). | [optional]
**image_url** | Option<**String**> | Publicly reachable http(s) image rendered large above the card. | [optional]
**buttons** | Option<[**Vec<models::CommentAutomationTemplateElementButtonsInner>**](CommentAutomationTemplateElementButtonsInner.md)> | Up to 3 card buttons. A generic template has NO phone button, on either platform. `url` buttons are click-tracked when linkTracking is on. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


