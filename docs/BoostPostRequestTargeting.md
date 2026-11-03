# BoostPostRequestTargeting

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**age_min** | Option<**i32**> |  | [optional]
**age_max** | Option<**i32**> |  | [optional]
**gender** | Option<**Gender**> | Applied on Meta, TikTok, Pinterest and Reddit. Ignored on Google, LinkedIn and X. (enum: all, male, female) | [optional]
**languages** | Option<**Vec<String>**> | Language codes, the same format as `languages` on POST /v1/ads/create.  - Meta: ISO 639-1 codes. A bare code targets all regional variants (\"en\" = all English); use a region-qualified code for a specific one (\"en_GB\", \"pt_BR\"). Meta numeric locale ids (e.g. \"24\" for English UK) are also accepted. Unknown values are rejected. - Reddit: ISO 639-1 codes (e.g. `en`). | [optional]
**countries** | Option<**Vec<String>**> | ISO country codes. Required for TikTok boosts (TikTok's ad group requires location_ids); optional on other platforms. | [optional]
**regions** | Option<[**Vec<models::UpdateCampaignTargetingRequestTargetingLocationsOneOfRegionsInnerOneOf>**](UpdateCampaignTargetingRequestTargetingLocationsOneOfRegionsInnerOneOf.md)> | Region/state targeting. `key` from /v1/ads/targeting/search?dimension=geo&geoType=region. | [optional]
**cities** | Option<[**Vec<models::BoostPostRequestTargetingCitiesInner>**](BoostPostRequestTargetingCitiesInner.md)> | City targeting. Optional `radius` + `distanceUnit` extend beyond the city limits (both set together, Meta only). | [optional]
**zips** | Option<[**Vec<models::UpdateCampaignTargetingRequestTargetingLocationsOneOfRegionsInnerOneOf>**](UpdateCampaignTargetingRequestTargetingLocationsOneOfRegionsInnerOneOf.md)> | Postal/ZIP targeting. `key` is the platform's postal location ID (e.g. Meta `US:94304`). | [optional]
**metros** | Option<[**Vec<models::UpdateCampaignTargetingRequestTargetingLocationsOneOfRegionsInnerOneOf>**](UpdateCampaignTargetingRequestTargetingLocationsOneOfRegionsInnerOneOf.md)> | DMA / metro-area targeting. `key` is the platform's metro ID (e.g. Meta `DMA:807`). | [optional]
**custom_locations** | Option<[**Vec<models::BoostPostRequestTargetingCustomLocationsInner>**](BoostPostRequestTargetingCustomLocationsInner.md)> | Point-radius (lat/lng) targeting (Meta custom_locations). No geo `key` lookup needed. | [optional]
**interests** | Option<[**Vec<models::UpdateAdRequestTargetingInterestsInner>**](UpdateAdRequestTargetingInterestsInner.md)> | Interest objects from /v1/ads/interests. Each must include id and name. | [optional]
**advantage_audience** | Option<**AdvantageAudience**> | Meta only. 0 = disabled (default), 1 = enabled. (enum: 0, 1) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


