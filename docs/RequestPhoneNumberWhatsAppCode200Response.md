# RequestPhoneNumberWhatsAppCode200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | Option<**String**> |  | [optional]
**method** | Option<**Method**> |  (enum: SMS, VOICE) | [optional]
**already_verified** | Option<**bool**> | Meta already reports the number as verified. No code is sent and the number is activated. | [optional]
**replaced** | Option<**bool**> | Meta refused the original number, which had never been live, so it was replaced on the same record. | [optional]
**new_phone_number** | Option<**String**> | The replacement number, present when `replaced` is true. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


