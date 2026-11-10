# ForwardEmailRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** |  | 
**to** | [**Vec<models::EmailAddress>**](EmailAddress.md) |  | 
**cc** | Option<[**Vec<models::EmailAddress>**](EmailAddress.md)> |  | [optional]
**bcc** | Option<[**Vec<models::EmailAddress>**](EmailAddress.md)> |  | [optional]
**reply_to** | Option<[**Vec<models::EmailAddress>**](EmailAddress.md)> |  | [optional]
**from_name** | Option<**String**> |  | [optional]
**from** | Option<**String**> | Send from another address of the mailbox, as on `POST /v1/email/messages`. | [optional]
**append_signature** | Option<**bool**> | Appends the signature of the sending address to the note, above the forwarded original: its Zernio default first, else its Gmail signature. | [optional]
**signature_id** | Option<**String**> | Appends this Zernio signature to the note instead. Wins over `appendSignature`. | [optional]
**subject** | Option<**String**> | Defaults to \"Fwd: \" plus the original subject. | [optional]
**text** | Option<**String**> | Optional note above the forwarded mail. | [optional]
**html** | Option<**String**> | Optional note above the forwarded mail, as html. | [optional]
**attachments** | Option<[**Vec<models::EmailAttachmentInput>**](EmailAttachmentInput.md)> | Added to the forwarded attachments. Everything together stays under 25 MB, else 413 `attachment_too_large`. | [optional]
**include_attachments** | Option<**bool**> | False keeps only the inline images of the original. | [optional][default to true]
**exclude_attachment_ids** | Option<**Vec<String>**> | Attachment ids (from a read of the original) to leave out. | [optional]
**metadata** | Option<**std::collections::HashMap<String, String>**> |  | [optional]
**track_opens** | Option<**bool**> | Adds an open pixel to the note and fires `email.opened`. Needs `html`. | [optional]
**track_links** | Option<**bool**> | Rewrites the links of the note and fires `email.link_clicked`. Needs `html`. | [optional]
**track_replies** | Option<**bool**> | Fires `email.thread_replied` when someone else writes in the thread. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


