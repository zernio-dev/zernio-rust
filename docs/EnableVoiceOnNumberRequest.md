# EnableVoiceOnNumberRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**forward_to** | Option<**String**> | tel:+E164, sip:..., or wss://... destination for inbound calls. Empty string clears the forward (outbound-only); omitted preserves the current one. | [optional]
**recording_enabled** | Option<**bool**> |  | [optional]
**transcription_enabled** | Option<**bool**> |  | [optional]
**transcription_language** | Option<**TranscriptionLanguage**> |  (enum: auto, en, es) | [optional]
**voicemail_enabled** | Option<**bool**> | Voicemail is taken when there's no live destination. Default on. | [optional]
**voicemail_greeting** | Option<**String**> | Custom spoken greeting; empty string restores the default. | [optional]
**business_hours_enabled** | Option<**bool**> | Outside the windows, inbound skips the forward and goes to voicemail. Off = 24/7. | [optional]
**business_hours_timezone** | Option<**String**> | IANA timezone the windows are evaluated in. | [optional]
**business_hours** | Option<[**Vec<models::EnableVoiceOnNumberRequestBusinessHoursInner>**](EnableVoiceOnNumberRequestBusinessHoursInner.md)> |  | [optional]
**blocked_callers** | Option<**Vec<String>**> | E.164 numbers rejected before answer. Replaces the whole list; bare 10-digit values are normalized as US numbers. | [optional]
**forward_caller_id** | Option<**ForwardCallerId**> | Caller ID on the forwarded leg: your number (`business`) or the original caller's (`caller`). (enum: business, caller) | [optional]
**ivr_enabled** | Option<**bool**> | IVR menu (supersedes the plain forward within business hours). | [optional]
**ivr_prompt** | Option<**String**> |  | [optional]
**ivr_options** | Option<[**Vec<models::EnableVoiceOnNumberRequestIvrOptionsInner>**](EnableVoiceOnNumberRequestIvrOptionsInner.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


