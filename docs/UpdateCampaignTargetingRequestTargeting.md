# UpdateCampaignTargetingRequestTargeting

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**devices** | Option<[**Vec<models::UpdateCampaignTargetingRequestTargetingDevicesInner>**](UpdateCampaignTargetingRequestTargetingDevicesInner.md)> | Devices to include. Devices not listed become excluded (negative) criteria, same contract as the existing devices-only edit. | [optional]
**locations** | Option<[**models::UpdateCampaignTargetingRequestTargetingLocations**](UpdateCampaignTargetingRequestTargetingLocations.md)> |  | [optional]
**languages** | Option<**Vec<String>**> | Google's language codes (ISO 639-1, plus variants such as `zh_CN`), e.g. [\"en\", \"de\"]. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


