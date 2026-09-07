# UpdateCampaignTargeting200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**campaign_id** | Option<**String**> |  | [optional]
**updated** | Option<**Vec<Updated>**> | Which targeting fields were applied. (enum: devices, locations, languages) | [optional]
**devices** | Option<[**Vec<models::UpdateCampaignTargeting200ResponseDevicesInner>**](UpdateCampaignTargeting200ResponseDevicesInner.md)> |  | [optional]
**locations** | Option<[**Vec<models::GetCampaignTargeting200ResponseLocationsInner>**](GetCampaignTargeting200ResponseLocationsInner.md)> |  | [optional]
**languages** | Option<[**Vec<models::UpdateCampaignTargeting200ResponseLanguagesInner>**](UpdateCampaignTargeting200ResponseLanguagesInner.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


