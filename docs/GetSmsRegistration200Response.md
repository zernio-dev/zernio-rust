# GetSmsRegistration200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**registration_type** | Option<**RegistrationType**> |  (enum: standard_10dlc, sole_prop_10dlc, toll_free) | [optional]
**status** | Option<**Status**> |  (enum: pending, approved, rejected) | [optional]
**brand_status** | Option<**String**> |  | [optional]
**campaign_status** | Option<**String**> |  | [optional]
**decline_reason** | Option<**String**> |  | [optional]
**phone_numbers** | Option<**Vec<String>**> |  | [optional]
**awaiting_otp** | Option<**bool**> |  | [optional]
**campaign_content** | Option<[**models::GetSmsRegistration200ResponseCampaignContent**](GetSmsRegistration200ResponseCampaignContent.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


