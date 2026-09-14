# TargetingSpecExcludedLocations

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**countries** | Option<**Vec<String>**> |  | [optional]
**country_groups** | Option<**Vec<CountryGroups>**> | Meta only. Continents and trade blocs to exclude (`excluded_geo_locations.country_groups`). (enum: africa, asia, europe, north_america, south_america, oceania, central_america, caribbean, eea, euro_area, nafta, mercosur, afta, apec, gcc, cisfta, emerging_markets, itunes_app_store, android_free_store, android_paid_store) | [optional]
**regions** | Option<[**Vec<models::UpdateCampaignTargetingRequestTargetingLocationsOneOfRegionsInner>**](UpdateCampaignTargetingRequestTargetingLocationsOneOfRegionsInner.md)> |  | [optional]
**cities** | Option<[**Vec<models::TargetingSpecExcludedLocationsCitiesInner>**](TargetingSpecExcludedLocationsCitiesInner.md)> | Cities to exclude. Optional `radius` + `distanceUnit` exclude a catchment around the city (both must be set together or both omitted); Meta honours the radius on excluded cities. | [optional]
**zips** | Option<[**Vec<models::UpdateCampaignTargetingRequestTargetingLocationsOneOfRegionsInner>**](UpdateCampaignTargetingRequestTargetingLocationsOneOfRegionsInner.md)> |  | [optional]
**places** | Option<[**Vec<models::TargetingSpecExcludedLocationsPlacesInner>**](TargetingSpecExcludedLocationsPlacesInner.md)> | Named points of interest to exclude. `key` from /v1/ads/targeting/search. | [optional]
**neighborhoods** | Option<[**Vec<models::TargetingSpecExcludedLocationsPlacesInner>**](TargetingSpecExcludedLocationsPlacesInner.md)> | Named neighbourhood areas to exclude. `key` from /v1/ads/targeting/search. | [optional]
**custom_locations** | Option<[**Vec<models::TargetingSpecCustomLocationsInner>**](TargetingSpecCustomLocationsInner.md)> | Point-radius (lat/lng) pins to exclude (Meta excluded_geo_locations.custom_locations). Mirrors the inclusion customLocations shape. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


