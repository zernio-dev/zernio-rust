# GetCampaignTargeting200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**devices** | Option<[**Vec<models::GetCampaignTargeting200ResponseDevicesInner>**](GetCampaignTargeting200ResponseDevicesInner.md)> |  | [optional]
**locations** | Option<[**Vec<models::GetCampaignTargeting200ResponseLocationsInner>**](GetCampaignTargeting200ResponseLocationsInner.md)> |  | [optional]
**languages** | Option<[**Vec<models::GetCampaignTargeting200ResponseLanguagesInner>**](GetCampaignTargeting200ResponseLanguagesInner.md)> |  | [optional]
**cached_at** | Option<**String**> | When this targeting was fetched from Google. Null when it was never served from cache. | [optional]
**stale** | Option<**bool**> | True when Google's daily API quota was exhausted and this is the last successful fetch, not a live read. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


