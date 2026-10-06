# CreateBroadcastRequestMessage

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | Option<**String**> | Required on every platform except WhatsApp (which sends `template`) and an SMS broadcast that carries attachments. | [optional]
**attachments** | Option<[**Vec<models::CreateBroadcastRequestMessageAttachmentsInner>**](CreateBroadcastRequestMessageAttachmentsInner.md)> | SMS only: sent as MMS media, one media_url per attachment. Each url must be public http(s); JPEG, PNG, GIF, WEBP, MP4 or 3GPP under 1 MB (checked at create when the host answers a HEAD request; Telnyx enforces the 1 MB total per message at send). | [optional]
**message_tag** | Option<**MessageTag**> | Instagram and Facebook only. Meta message tag sent with every recipient message (messaging_type MESSAGE_TAG) so the broadcast can reach people outside the 24h window. Instagram accepts HUMAN_AGENT only. Rejected with a 400 on any other platform. (enum: CONFIRMED_EVENT_UPDATE, POST_PURCHASE_UPDATE, ACCOUNT_UPDATE, HUMAN_AGENT) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


