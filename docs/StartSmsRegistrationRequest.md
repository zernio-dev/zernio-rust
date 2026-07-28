# StartSmsRegistrationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**registration_type** | **RegistrationType** |  (enum: standard_10dlc, sole_prop_10dlc, toll_free) | 
**phone_numbers** | **Vec<String>** | Your numbers this registration covers. | 
**brand** | Option<[**models::StartSmsRegistrationRequestBrand**](StartSmsRegistrationRequestBrand.md)> |  | [optional]
**campaign** | Option<[**models::StartSmsRegistrationRequestCampaign**](StartSmsRegistrationRequestCampaign.md)> |  | [optional]
**messaging_brand_name** | Option<**String**> | DBA / trade name used to brand message content (samples and auto-replies) when it differs from the legal name, e.g. a sole proprietor texting under a business name. The legal `brand.displayName` is still what the carrier vets. | [optional]
**wizard_values** | Option<**std::collections::HashMap<String, String>**> | Raw dashboard-wizard answers, stored only to prefill edit-and-resubmit. API integrators can omit. | [optional]
**resubmit_request_id** | Option<**String**> | Resubmit a registration that was returned for changes — updates it in place instead of creating a new one. | [optional]
**toll_free** | Option<[**models::StartSmsRegistrationRequestTollFree**](StartSmsRegistrationRequestTollFree.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


