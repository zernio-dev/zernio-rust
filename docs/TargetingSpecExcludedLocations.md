# TargetingSpecExcludedLocations

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**countries** | Option<**Vec<String>**> |  | [optional]
**regions** | Option<[**Vec<models::BoostPostRequestTargetingRegionsInner>**](BoostPostRequestTargetingRegionsInner.md)> |  | [optional]
**cities** | Option<[**Vec<models::TargetingSpecExcludedLocationsCitiesInner>**](TargetingSpecExcludedLocationsCitiesInner.md)> | Cities to exclude. Optional `radius` + `distanceUnit` exclude a catchment around the city (both must be set together or both omitted); Meta honours the radius on excluded cities. | [optional]
**zips** | Option<[**Vec<models::BoostPostRequestTargetingRegionsInner>**](BoostPostRequestTargetingRegionsInner.md)> |  | [optional]
**places** | Option<[**Vec<models::TargetingSpecExcludedLocationsPlacesInner>**](TargetingSpecExcludedLocationsPlacesInner.md)> | Named points of interest to exclude. `key` from /v1/ads/targeting/search. | [optional]
**neighborhoods** | Option<[**Vec<models::TargetingSpecExcludedLocationsPlacesInner>**](TargetingSpecExcludedLocationsPlacesInner.md)> | Named neighbourhood areas to exclude. `key` from /v1/ads/targeting/search. | [optional]
**custom_locations** | Option<[**Vec<models::TargetingSpecCustomLocationsInner>**](TargetingSpecCustomLocationsInner.md)> | Point-radius (lat/lng) pins to exclude (Meta excluded_geo_locations.custom_locations). Mirrors the inclusion customLocations shape. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


