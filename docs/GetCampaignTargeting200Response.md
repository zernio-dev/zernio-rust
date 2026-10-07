# GetCampaignTargeting200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**devices** | Option<[**Vec<models::GetCampaignTargeting200ResponseDevicesInner>**](GetCampaignTargeting200ResponseDevicesInner.md)> |  | [optional]
**locations** | Option<[**Vec<models::GetCampaignTargeting200ResponseLocationsInner>**](GetCampaignTargeting200ResponseLocationsInner.md)> |  | [optional]
**excluded_locations** | Option<[**Vec<models::GetCampaignTargeting200ResponseExcludedLocationsInner>**](GetCampaignTargeting200ResponseExcludedLocationsInner.md)> | The negative (excluded) location criteria, same item shape as `locations` with `negative: true`. | [optional]
**excluded_locations_editable** | Option<**bool**> | Whether PUT accepts `excludedLocations` for this campaign. False on Demand Gen, which returns 400 for any exclusion. | [optional]
**languages** | Option<[**Vec<models::GetCampaignTargeting200ResponseLanguagesInner>**](GetCampaignTargeting200ResponseLanguagesInner.md)> |  | [optional]
**location_targeting_type** | Option<**LocationTargetingType**> | Who the location targeting reaches, see GoogleLocationTargetingType. Null when Google reports a legacy value (SEARCH_INTEREST) this API does not set. (enum: presence, presence_or_interest, ) | [optional]
**cached_at** | Option<**String**> | When this targeting was fetched from Google. Null when it was never served from cache. | [optional]
**stale** | Option<**bool**> | True when Google's daily API quota was exhausted and this is the last successful fetch, not a live read. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


