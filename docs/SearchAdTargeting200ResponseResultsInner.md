# SearchAdTargeting200ResponseResultsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | The platform's opaque id. Use as a geo `key` (regions/cities/zips/metros) or an entity `id` (interests/behaviors) in TargetingSpec. A `country` result is the exception on every platform: its id is the ISO 3166-1 alpha-2 code, which is what `targeting.countries` takes. | 
**name** | **String** | Human-readable label. | 
**r#type** | **String** | What the result is (e.g. city, region, country, zip, metro, location, interest, behavior, income, industry, jobFunction, seniority, companySize). | 
**path** | Option<**Vec<String>**> | Optional breadcrumb of parent labels (e.g. ['United States', 'California', 'Los Angeles']). Disambiguates same-named results. | [optional]
**audience_size** | Option<**i32**> | Optional estimated reachable users for this option, when the platform returns it. | [optional]
**country_code** | Option<**String**> | ISO-3166 alpha-2 of the country a sub-country geo result (city, region, zip, metro) belongs to, when the platform reports it (Meta does). Useful to know whether a location falls under the EU DSA disclosure rules before creating the ad. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


