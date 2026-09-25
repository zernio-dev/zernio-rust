# GetPhoneNumberClaim200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**country** | Option<[**models::GetPhoneNumberClaim200ResponseCountry**](GetPhoneNumberClaim200ResponseCountry.md)> |  | [optional]
**r#type** | Option<**serde_json::Value**> | The claimed number type, in the shape of `types[]` on GET /v1/phone-numbers/countries. | [optional]
**area** | Option<[**models::GetPhoneNumberClaim200ResponseArea**](GetPhoneNumberClaim200ResponseArea.md)> |  | [optional]
**phone_number** | Option<**String**> | E.164, or null for an any-number claim. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


