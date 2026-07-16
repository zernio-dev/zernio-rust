# BoostPostRequestTargeting

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**age_min** | Option<**i32**> |  | [optional]
**age_max** | Option<**i32**> |  | [optional]
**gender** | Option<**Gender**> | Meta only. (enum: all, male, female) | [optional]
**languages** | Option<**Vec<String>**> | Meta locale ids (numeric), passed through as given. | [optional]
**countries** | Option<**Vec<String>**> | ISO country codes. Required for TikTok boosts (TikTok's ad group requires location_ids); optional on other platforms. | [optional]
**regions** | Option<[**Vec<models::BoostPostRequestTargetingRegionsInner>**](BoostPostRequestTargetingRegionsInner.md)> | Region/state targeting. `key` from /v1/ads/targeting/search?dimension=geo&geoType=region. | [optional]
**cities** | Option<[**Vec<models::BoostPostRequestTargetingCitiesInner>**](BoostPostRequestTargetingCitiesInner.md)> | City targeting. Optional `radius` + `distance_unit` extend beyond the city limits (both set together, Meta only). | [optional]
**zips** | Option<[**Vec<models::BoostPostRequestTargetingRegionsInner>**](BoostPostRequestTargetingRegionsInner.md)> | Postal/ZIP targeting. `key` is the platform's postal location ID (e.g. Meta `US:94304`). | [optional]
**metros** | Option<[**Vec<models::BoostPostRequestTargetingRegionsInner>**](BoostPostRequestTargetingRegionsInner.md)> | DMA / metro-area targeting. `key` is the platform's metro ID (e.g. Meta `DMA:807`). | [optional]
**custom_locations** | Option<[**Vec<models::BoostPostRequestTargetingCustomLocationsInner>**](BoostPostRequestTargetingCustomLocationsInner.md)> | Point-radius (lat/lng) targeting (Meta custom_locations). No geo `key` lookup needed. | [optional]
**interests** | Option<[**Vec<models::UpdateAdRequestTargetingInterestsInner>**](UpdateAdRequestTargetingInterestsInner.md)> | Interest objects from /v1/ads/interests. Each must include id and name. | [optional]
**advantage_audience** | Option<**AdvantageAudience**> | Meta only. 0 = disabled (default), 1 = enabled. (enum: 0, 1) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


