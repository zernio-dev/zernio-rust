# EmailMessage

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | The provider's message id. | [optional]
**thread_id** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**provider** | Option<**Provider**> |  (enum: google, microsoft) | [optional]
**folders** | Option<**Vec<String>**> |  | [optional]
**from** | Option<[**models::EmailAddress**](EmailAddress.md)> |  | [optional]
**to** | Option<[**Vec<models::EmailAddress>**](EmailAddress.md)> |  | [optional]
**cc** | Option<[**Vec<models::EmailAddress>**](EmailAddress.md)> |  | [optional]
**bcc** | Option<[**Vec<models::EmailAddress>**](EmailAddress.md)> |  | [optional]
**reply_to** | Option<[**Vec<models::EmailAddress>**](EmailAddress.md)> |  | [optional]
**subject** | Option<**String**> |  | [optional]
**snippet** | Option<**String**> |  | [optional]
**text** | Option<**String**> |  | [optional]
**html** | Option<**String**> |  | [optional]
**attachments** | Option<[**Vec<models::EmailAttachment>**](EmailAttachment.md)> |  | [optional]
**headers** | Option<**std::collections::HashMap<String, String>**> | Only with `includeHeaders=true`. | [optional]
**raw** | Option<**String**> | MIME source, only with `raw=true`. | [optional]
**date** | Option<**String**> |  | [optional]
**unread** | Option<**bool**> |  | [optional]
**starred** | Option<**bool**> |  | [optional]
**labels** | Option<**Vec<String>**> | Gmail: the ids of the user labels on the message (names come from `GET /v1/email/labels`). Outlook: its category names. | [optional]
**metadata** | Option<**std::collections::HashMap<String, String>**> |  | [optional]
**tracking_id** | Option<**String**> | Set on a send with `trackOpens`, `trackLinks` or `trackReplies`; the email.* webhooks carry it. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


