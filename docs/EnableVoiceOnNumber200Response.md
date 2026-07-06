# EnableVoiceOnNumber200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | Option<**bool**> |  | [optional]
**phone_number** | Option<**String**> |  | [optional]
**pstn_forward_to** | Option<**String**> |  | [optional]
**recording_enabled** | Option<**bool**> |  | [optional]
**transcription_enabled** | Option<**bool**> |  | [optional]
**transcription_language** | Option<**TranscriptionLanguage**> |  (enum: auto, en, es) | [optional]
**voicemail_enabled** | Option<**bool**> |  | [optional]
**voicemail_greeting** | Option<**String**> |  | [optional]
**business_hours_enabled** | Option<**bool**> |  | [optional]
**business_hours_timezone** | Option<**String**> |  | [optional]
**business_hours** | Option<[**Vec<models::EnableVoiceOnNumber200ResponseBusinessHoursInner>**](EnableVoiceOnNumber200ResponseBusinessHoursInner.md)> |  | [optional]
**blocked_callers** | Option<**Vec<String>**> |  | [optional]
**forward_caller_id** | Option<**ForwardCallerId**> |  (enum: business, caller) | [optional]
**ivr_enabled** | Option<**bool**> |  | [optional]
**ivr_prompt** | Option<**String**> |  | [optional]
**ivr_options** | Option<[**Vec<models::EnableVoiceOnNumber200ResponseIvrOptionsInner>**](EnableVoiceOnNumber200ResponseIvrOptionsInner.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


