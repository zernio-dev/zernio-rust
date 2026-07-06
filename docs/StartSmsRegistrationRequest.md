# StartSmsRegistrationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**registration_type** | **RegistrationType** |  (enum: standard_10dlc, sole_prop_10dlc, toll_free) | 
**phone_numbers** | **Vec<String>** | Your numbers this registration covers. | 
**brand** | Option<[**models::StartSmsRegistrationRequestBrand**](StartSmsRegistrationRequestBrand.md)> |  | [optional]
**campaign** | Option<[**models::StartSmsRegistrationRequestCampaign**](StartSmsRegistrationRequestCampaign.md)> |  | [optional]
**toll_free** | Option<[**models::StartSmsRegistrationRequestTollFree**](StartSmsRegistrationRequestTollFree.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


