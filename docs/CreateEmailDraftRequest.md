# CreateEmailDraftRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** |  | 
**to** | Option<[**Vec<models::EmailAddress>**](EmailAddress.md)> | Optional on a draft; needed before it is sent. | [optional]
**cc** | Option<[**Vec<models::EmailAddress>**](EmailAddress.md)> |  | [optional]
**bcc** | Option<[**Vec<models::EmailAddress>**](EmailAddress.md)> |  | [optional]
**reply_to** | Option<[**Vec<models::EmailAddress>**](EmailAddress.md)> |  | [optional]
**from_name** | Option<**String**> |  | [optional]
**from** | Option<**String**> | Send from another address of the mailbox, as on `POST /v1/email/messages`. Checked when the draft is saved. | [optional]
**append_signature** | Option<**bool**> | Puts the signature of the sending address in the draft body, where the user sees it: its Zernio default first, else its Gmail signature. | [optional]
**signature_id** | Option<**String**> | Puts this Zernio signature in the draft body instead. Wins over `appendSignature`. | [optional]
**subject** | Option<**String**> | On a reply draft, empty keeps the thread subject. | [optional]
**text** | Option<**String**> |  | [optional]
**html** | Option<**String**> |  | [optional]
**attachments** | Option<[**Vec<models::EmailAttachmentInput>**](EmailAttachmentInput.md)> |  | [optional]
**headers** | Option<**std::collections::HashMap<String, String>**> | Custom `X-` headers only. | [optional]
**metadata** | Option<**std::collections::HashMap<String, String>**> | Kept with the draft and returned on the sent message and its email.* webhooks. | [optional]
**in_reply_to** | Option<**String**> | Makes a reply draft in that message's thread, addressed and threaded like a reply. Not with `forwardOf`. | [optional]
**reply_all** | Option<**bool**> | With `inReplyTo`: address every recipient of the original. Leave out `to`, `cc` and `bcc`. | [optional]
**forward_of** | Option<**String**> | Makes a forward draft of that message, with its attachments. Recipients can come later. Not with `inReplyTo`. | [optional]
**include_attachments** | Option<**bool**> | With `forwardOf`: false keeps only the inline images of the original. | [optional][default to true]
**exclude_attachment_ids** | Option<**Vec<String>**> | With `forwardOf`: attachment ids (from a read of the original) to leave out. | [optional]
**track_opens** | Option<**bool**> | Puts the open pixel in the draft html now; fires `email.opened` once it is sent. Needs `html`. | [optional]
**track_links** | Option<**bool**> | Rewrites the draft's links now; fires `email.link_clicked` once it is sent. Needs `html`. | [optional]
**track_replies** | Option<**bool**> | Fires `email.thread_replied` once it is sent. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


