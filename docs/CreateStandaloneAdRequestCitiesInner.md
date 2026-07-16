# CreateStandaloneAdRequestCitiesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **String** | Meta city ID, from /v1/ads/targeting/search results. | 
**radius** | Option<**f64**> | Optional radius around the city. Must be set together with distance_unit. Meta enforces a minimum city radius (~17 km / 10 mi); smaller values resolve to a 0-size audience and the ad fails at launch. For a tighter catchment use customLocations (lat/lng). | [optional]
**distance_unit** | Option<**DistanceUnit**> | Unit for radius. Required if radius is set. (enum: mile, kilometer) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


