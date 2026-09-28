# CreateRcsAgentRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** |  | 
**brand_id** | Option<**String**> |  | [optional]
**brand** | Option<[**models::RcsBrandInput**](RcsBrandInput.md)> |  | [optional]
**display_name** | **String** | Shown as the sender name. | 
**use_case** | **UseCase** |  (enum: MULTI_USE, PROMOTIONAL, TRANSACTIONAL, OTP) | 
**profile** | [**models::RcsAgentProfile**](RcsAgentProfile.md) |  | 
**sms_fallback_from** | Option<**String**> | One of your SMS-enabled numbers. Phones without RCS get the message as SMS from it. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


