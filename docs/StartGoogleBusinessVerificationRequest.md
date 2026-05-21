# StartGoogleBusinessVerificationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**method** | **Method** | The verification method. Selects which method-specific field below is required. (enum: ADDRESS, EMAIL, PHONE_CALL, SMS, AUTO, VETTED_PARTNER) | 
**language_code** | Option<**String**> |  | [optional]
**phone_number** | Option<**String**> | For PHONE_CALL / SMS. | [optional]
**email_address** | Option<**String**> | For EMAIL. | [optional]
**mailer_contact** | Option<**serde_json::Value**> | For ADDRESS (postcard) verification. | [optional]
**context** | Option<**serde_json::Value**> | ServiceBusinessContext (e.g. service address). Required for service-area businesses. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


