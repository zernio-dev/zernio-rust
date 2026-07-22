# CreateVerificationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channel** | **Channel** | SMS-only for now. (enum: sms) | 
**to** | **String** | E.164 phone number. | 
**from** | Option<**String**> | The SMS-enabled number on your account to send from. Defaults to your only SMS number. | [optional]
**brand_name** | Option<**String**> | Your app or business name, rendered in the message. Defaults to your account name. Letters, numbers, and basic punctuation only. | [optional]
**code_length** | Option<**i32**> |  | [optional][default to 6]
**ttl_minutes** | Option<**i32**> |  | [optional][default to 10]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


