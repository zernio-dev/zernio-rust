# DialVoiceWebCallRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**to** | **String** | The number to call, E.164 with leading +. | 
**credential_id** | **String** | The WebRTC credential id returned by POST /v1/voice/calls/web (the registered browser). | 
**from_number** | Option<**String**> | Which of your voice-enabled numbers to call from (optional when you have one). | [optional]
**record_override** | Option<**bool**> |  | [optional]
**ring_timeout_seconds** | Option<**i32**> | Seconds to let the callee's phone ring before the call ends as no_answer. The destination carrier can end it sooner. | [optional][default to 30]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


