# CreateVerificationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channel** | **Channel** |  (enum: sms, whatsapp) | 
**to** | **String** | E.164 phone number. WhatsApp only delivers to a phone number, never to a username. | 
**from** | Option<**String**> | The number on your account to send from: an SMS-enabled number for `sms`, a connected WhatsApp number for `whatsapp`. Defaults to your only number on that channel. | [optional]
**brand_name** | Option<**String**> | Your app or business name, rendered in the SMS message. Defaults to your account name. Not shown on WhatsApp, where Meta fixes the message and shows your WhatsApp display name. Letters, numbers, and basic punctuation only. | [optional]
**code_length** | Option<**i32**> |  | [optional][default to 6]
**ttl_minutes** | Option<**i32**> |  | [optional][default to 10]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


