# TargetingSpec

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**countries** | Option<**Vec<String>**> | ISO 3166-1 alpha-2 country codes (e.g. ['US']). | [optional]
**regions** | Option<[**Vec<models::BoostPostRequestTargetingRegionsInner>**](BoostPostRequestTargetingRegionsInner.md)> | Region/state targeting. `key` is the platform location ID from /v1/ads/targeting/search?dimension=geo&geoType=region. | [optional]
**cities** | Option<[**Vec<models::TargetingSpecCitiesInner>**](TargetingSpecCitiesInner.md)> | City targeting. Optional `radius` + `distanceUnit` extend beyond the city limits; both must be set together or both omitted. `radius` is only honoured on platforms whose capability map allows city radius (Meta). | [optional]
**zips** | Option<[**Vec<models::BoostPostRequestTargetingRegionsInner>**](BoostPostRequestTargetingRegionsInner.md)> | Postal/ZIP targeting. `key` is the platform's postal location ID (e.g. Meta `US:94304`). Supported on Meta, Google, TikTok, Pinterest, X. | [optional]
**metros** | Option<[**Vec<models::BoostPostRequestTargetingRegionsInner>**](BoostPostRequestTargetingRegionsInner.md)> | DMA / metro-area targeting. `key` is the platform's metro ID (e.g. Meta `DMA:807`). | [optional]
**custom_locations** | Option<[**Vec<models::TargetingSpecCustomLocationsInner>**](TargetingSpecCustomLocationsInner.md)> | Point-radius (lat/lng) targeting (Meta custom_locations / Google proximity). Honoured only where the capability map allows radius (Meta). | [optional]
**excluded_locations** | Option<[**models::TargetingSpecExcludedLocations**](TargetingSpecExcludedLocations.md)> |  | [optional]
**age_min** | Option<**i32**> |  | [optional]
**age_max** | Option<**i32**> |  | [optional]
**gender** | Option<**Gender**> | Restrict by gender. 'all' (default) targets everyone. (enum: all, male, female) | [optional]
**income_tier** | Option<**IncomeTier**> | Normalized household-income tier (ZIP/percentile based). Meta and TikTok express all four. Google maps only `top_10` (its INCOME_RANGE_90_UP); other tiers on Google, and any income tier on LinkedIn / X / Pinterest, are rejected. On Meta, income/zip targeting requires the relevant `specialAdCategories` to be unset (housing/employment/credit ads cannot use it).  (enum: top_5, top_10, top_10_25, top_25_50) | [optional]
**languages** | Option<**Vec<String>**> | Language codes (e.g. ['en']). | [optional]
**interests** | Option<[**Vec<models::CreateStandaloneAdRequestBehaviorsInner>**](CreateStandaloneAdRequestBehaviorsInner.md)> | Interest entities from /v1/ads/targeting/search?dimension=interest. Each carries the platform's opaque id. | [optional]
**behaviors** | Option<[**Vec<models::CreateStandaloneAdRequestBehaviorsInner>**](CreateStandaloneAdRequestBehaviorsInner.md)> | Behaviour entities from /v1/ads/targeting/search?dimension=behavior. Supported on Meta and TikTok. | [optional]
**industries** | Option<**Vec<String>**> | LinkedIn B2B only. Industry URN id fragments. | [optional]
**company_sizes** | Option<**Vec<String>**> | LinkedIn B2B only. | [optional]
**seniorities** | Option<**Vec<String>**> | LinkedIn B2B only. | [optional]
**job_functions** | Option<**Vec<String>**> | LinkedIn B2B only. | [optional]
**audience_include** | Option<**Vec<String>**> | Platform audience IDs to include. | [optional]
**audience_exclude** | Option<**Vec<String>**> | Platform audience IDs to exclude. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


