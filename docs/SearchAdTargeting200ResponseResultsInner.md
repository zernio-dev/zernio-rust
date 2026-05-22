# SearchAdTargeting200ResponseResultsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | The platform's opaque id. Use as a geo `key` (regions/cities/zips/metros) or an entity `id` (interests/behaviors) in TargetingSpec. | 
**name** | **String** | Human-readable label. | 
**r#type** | **String** | What the result is (e.g. city, region, country, zip, metro, interest, behavior, income). | 
**path** | Option<**Vec<String>**> | Optional breadcrumb of parent labels (e.g. ['United States', 'California', 'Los Angeles']). Disambiguates same-named results. | [optional]
**audience_size** | Option<**i32**> | Optional estimated reachable users for this option, when the platform returns it. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


