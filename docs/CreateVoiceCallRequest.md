# CreateVoiceCallRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**to** | **String** | Destination to dial, E.164 with leading +. | 
**from_number** | Option<**String**> | Which of your voice-enabled numbers to dial from. Optional when you have exactly one. | [optional]
**forward_to** | Option<**String**> | Per-call agent override (tel:+E164, sip:..., or wss://...); defaults to the number's stored forward destination. | [optional]
**greeting** | Option<**String**> | Spoken to the callee when they answer, before the bridge. | [optional]
**record_override** | Option<**bool**> | Per-call recording toggle; defaults to the number's setting. | [optional]
**transcribe_override** | Option<**bool**> | Per-call transcription toggle; defaults to the number's setting. | [optional]
**transcription_language** | Option<**TranscriptionLanguage**> | 'auto' derives from the callee's country; 'en'/'es' force it. (enum: auto, en, es) | [optional]
**amd** | Option<**bool**> | Answering-machine detection; defers the bridge until human vs machine is known. | [optional]
**voicemail_drop_message** | Option<**String**> | Spoken to a detected machine, then hang up (implies `amd`). For outbound voicemail drops. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


