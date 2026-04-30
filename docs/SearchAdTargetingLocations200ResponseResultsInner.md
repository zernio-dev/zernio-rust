# SearchAdTargetingLocations200ResponseResultsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **String** | Meta's opaque location ID. Use this in targeting.cities[].key / regions[].key. | 
**name** | **String** |  | 
**r#type** | **String** | Location type as returned by Meta (city, region, country, etc.). | 
**country_code** | Option<**String**> |  | [optional]
**country_name** | Option<**String**> |  | [optional]
**region** | Option<**String**> | Parent region/state name (cities only). | [optional]
**region_id** | Option<[**models::SearchAdTargetingLocations200ResponseResultsInnerRegionId**](SearchAdTargetingLocations200ResponseResultsInnerRegionId.md)> |  | [optional]
**supports_region** | Option<**bool**> |  | [optional]
**supports_city** | Option<**bool**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


