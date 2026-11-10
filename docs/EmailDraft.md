# EmailDraft

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | The draft id: the Gmail draft id, or the Outlook message id. | [optional]
**thread_id** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**provider** | Option<**Provider**> |  (enum: google, microsoft) | [optional]
**folders** | Option<**Vec<String>**> |  | [optional]
**from** | Option<[**models::EmailAddress**](EmailAddress.md)> |  | [optional]
**sender** | Option<[**models::EmailAddress**](EmailAddress.md)> |  | [optional]
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
**tracking_id** | Option<**String**> | Set when the draft was created with tracking. | [optional]
**clean** | Option<[**models::EmailClean**](EmailClean.md)> |  | [optional]
**draft_id** | Option<**String**> | On a mail sent from a draft (`POST /v1/email/drafts/{draftId}/send`): the draft it was. The sent mail has a new id. | [optional]
**forwarded_from** | Option<**String**> | On a forward: the message it forwarded. | [optional]
**object** | Option<**Object**> |  (enum: draft) | [optional]
**kind** | Option<**Kind**> | Fixed when the draft is created. A draft the user wrote in their mail client is read from its headers. (enum: new, reply, forward) | [optional]
**version** | Option<**String**> | Changes on every edit, the user's in Gmail or Outlook included. Pass it as `If-Match` to update or send only that version. Also the `ETag` response header. | [optional]
**message_id** | Option<**String**> | The provider message behind the draft. Volatile: Gmail replaces it on every save. | [optional]
**in_reply_to** | Option<**String**> | The message a reply draft answers. | [optional]
**forward_of** | Option<**String**> | The message a forward draft forwards. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


