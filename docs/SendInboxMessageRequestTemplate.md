# SendInboxMessageRequestTemplate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | Option<**Type**> | Template type. Required for Instagram/Facebook generic templates; ignored on WhatsApp. (enum: generic) | [optional]
**image_aspect_ratio** | Option<**ImageAspectRatio**> | Facebook only. Aspect ratio Messenger renders element images at: horizontal (1.91:1, default) or square (1:1). A 400 on Instagram. (enum: horizontal, square) | [optional]
**elements** | Option<[**Vec<models::SendInboxMessageRequestTemplateElementsInner>**](SendInboxMessageRequestTemplateElementsInner.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


