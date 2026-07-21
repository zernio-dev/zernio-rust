# SendSmsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**from** | **String** | One of your SMS-enabled numbers (E.164; formatting is normalized), or an approved alphanumeric sender ID (3-11 letters/digits/spaces, created via `/v1/sms/sender-ids`). | 
**to** | **String** | Recipient number (E.164). | 
**text** | Option<**String**> | Message body. Required unless `mediaUrls` is set. Max 10 SMS segments (1530 GSM-7 or 670 unicode characters). | [optional]
**media_urls** | Option<**Vec<String>**> | Public media URLs to attach (sends as MMS). Max 10. | [optional]
**send_at** | Option<**String**> | Optional. Schedule the send for a future time (ISO 8601 with offset, e.g. `2026-08-01T12:00:00Z`). Must be in the future. The message is queued and the `message.delivered` webhook fires when it actually sends. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


