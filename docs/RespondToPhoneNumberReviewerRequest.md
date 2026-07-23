# RespondToPhoneNumberReviewerRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | Option<**String**> | Your message to the reviewer. | [optional]
**documents** | Option<[**Vec<models::RespondToPhoneNumberReviewerRequestDocumentsInner>**](RespondToPhoneNumberReviewerRequestDocumentsInner.md)> | Corrected requirement documents, each keyed to its requirement. | [optional]
**address** | Option<**serde_json::Value**> | A corrected address record, keyed to its requirement. | [optional]
**entity_type** | Option<**EntityType**> |  (enum: individual, business, ) | [optional]
**attachments** | Option<[**Vec<models::ReplyToPhoneNumberReviewerRequestAttachmentsInner>**](ReplyToPhoneNumberReviewerRequestAttachmentsInner.md)> | Loose files (PDF/JPG/PNG/WEBP, max 10 MB each) whose links are added to your message. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


