# UpdateEmailDraftRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** |  | 
**to** | Option<[**Vec<models::EmailAddress>**](EmailAddress.md)> |  | [optional]
**cc** | Option<[**Vec<models::EmailAddress>**](EmailAddress.md)> |  | [optional]
**bcc** | Option<[**Vec<models::EmailAddress>**](EmailAddress.md)> |  | [optional]
**reply_to** | Option<[**Vec<models::EmailAddress>**](EmailAddress.md)> |  | [optional]
**subject** | Option<**String**> |  | [optional]
**text** | Option<**String**> |  | [optional]
**html** | Option<**String**> | On a draft created with tracking, the new html is instrumented again under the same `trackingId`. | [optional]
**attachments** | Option<[**Vec<models::EmailAttachmentInput>**](EmailAttachmentInput.md)> |  | [optional]
**signature_id** | Option<**String**> | Swaps the Zernio signature block in the new `html` or `text` for this signature, so switching never stacks two; `null` removes it. Needs `html` or `text` in the same request. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


