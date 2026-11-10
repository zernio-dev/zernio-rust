# ReplyEmailMessageRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** |  | 
**to** | [**Vec<models::EmailAddress>**](EmailAddress.md) |  | 
**cc** | Option<[**Vec<models::EmailAddress>**](EmailAddress.md)> |  | [optional]
**bcc** | Option<[**Vec<models::EmailAddress>**](EmailAddress.md)> |  | [optional]
**reply_to** | Option<[**Vec<models::EmailAddress>**](EmailAddress.md)> |  | [optional]
**from_name** | Option<**String**> |  | [optional]
**from** | Option<**String**> | Send from another address listed by `GET /v1/email/send-as`; on Outlook, declare a shared mailbox there first. An address not on the list answers 400, and Outlook refusing it at send time answers 403. Omitted, the mail leaves from the mailbox address. | [optional]
**append_signature** | Option<**bool**> | Appends the signature of the sending address: its Zernio default first, else its Gmail signature. 400 when it has neither. | [optional]
**signature_id** | Option<**String**> | Appends this Zernio signature instead. Wins over `appendSignature`. | [optional]
**subject** | **String** | Optional on replies; the provider keeps the thread subject. | 
**text** | Option<**String**> | Plain-text body. One of `text` or `html` is required. | [optional]
**html** | Option<**String**> |  | [optional]
**attachments** | Option<[**Vec<models::SendEmailRequestAttachmentsInner>**](SendEmailRequestAttachmentsInner.md)> | 25 MB in total on every provider. Send files over 4 MB by url: request bodies are capped at 4.5 MB. | [optional]
**headers** | Option<**std::collections::HashMap<String, String>**> | Custom `X-` headers only. `List-Unsubscribe` is dropped on Microsoft and reported in `metadata.droppedHeaders`. | [optional]
**metadata** | Option<**std::collections::HashMap<String, String>**> |  | [optional]
**scheduled_for** | Option<**String**> | Send later, between 1 minute and 30 days from now. The request answers 202 with the scheduled send; it leaves within a minute of this time through the same caps as an immediate send. List or cancel it under `/v1/email/messages/scheduled`. | [optional]
**hold_as_draft** | Option<**bool**> | Needs `scheduledFor`. Saves the email as a draft in the mailbox now and sends that draft at `scheduledFor`, with any edits the user made in their mail app. A draft deleted or sent from the mailbox first fails the send (`email.send_failed`). Cancelling deletes the draft. | [optional]
**track_opens** | Option<**bool**> | Adds an open pixel to the html and fires `email.opened`. Needs `html`. | [optional]
**track_links** | Option<**bool**> | Rewrites every http(s) link in the html through a Zernio redirect and fires `email.link_clicked`. Needs `html`. | [optional]
**track_replies** | Option<**bool**> | Fires `email.thread_replied` when someone else writes in this message's thread. Works with text or html. | [optional]
**mode** | Option<**Mode**> |  (enum: reply, replyAll) | [optional][default to Reply]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


