# SendEmailRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** |  | 
**to** | [**Vec<models::EmailAddress>**](EmailAddress.md) |  | 
**cc** | Option<[**Vec<models::EmailAddress>**](EmailAddress.md)> |  | [optional]
**bcc** | Option<[**Vec<models::EmailAddress>**](EmailAddress.md)> |  | [optional]
**reply_to** | Option<[**Vec<models::EmailAddress>**](EmailAddress.md)> |  | [optional]
**from_name** | Option<**String**> |  | [optional]
**subject** | **String** |  | 
**text** | Option<**String**> | Plain-text body. One of `text` or `html` is required. | [optional]
**html** | Option<**String**> |  | [optional]
**attachments** | Option<[**Vec<models::SendEmailRequestAttachmentsInner>**](SendEmailRequestAttachmentsInner.md)> | 25 MB in total; 3 MB per attachment on Microsoft. | [optional]
**headers** | Option<**std::collections::HashMap<String, String>**> | Custom `X-` headers only. `List-Unsubscribe` is dropped on Microsoft and reported in `metadata.droppedHeaders`. | [optional]
**metadata** | Option<**std::collections::HashMap<String, String>**> |  | [optional]
**scheduled_for** | Option<**String**> | Reserved; currently rejected. | [optional]
**hold_as_draft** | Option<**bool**> | Reserved; currently rejected. | [optional]
**track_opens** | Option<**bool**> | Not available; must be false. | [optional]
**track_links** | Option<**bool**> | Not available; must be false. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


