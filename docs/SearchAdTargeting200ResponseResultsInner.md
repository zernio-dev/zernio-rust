# SearchAdTargeting200ResponseResultsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | The platform's opaque id. Use as a geo `key` (regions/cities/zips/metros) or an entity `id` (interests/behaviors) in TargetingSpec. A `country` result is the exception on every platform: its id is the ISO 3166-1 alpha-2 code, which is what `targeting.countries` takes. | 
**name** | **String** | Human-readable label. | 
**r#type** | **String** | What the result is. Equals the requested dimension (interest, interestKeyword, behavior, hashtag, income, language, workPosition, workEmployer, workIndustry, industry, jobFunction, seniority, companySize), or the location level for geo (country, region, city, zip, metro, ...). | 
**path** | Option<**Vec<String>**> | Optional breadcrumb of parent labels (e.g. ['United States', 'California', 'Los Angeles']). Disambiguates same-named results. | [optional]
**audience_size** | Option<**i32**> | Optional estimated reachable users for this option, when the platform returns it. | [optional]
**status** | Option<**String**> | TikTok `interestKeyword` and `hashtag` results only: TikTok's availability status. `EFFECTIVE` / `INEFFECTIVE` for additional interests, `ONLINE` / `OFFLINE` for hashtags. Only `EFFECTIVE` and `ONLINE` ids can be targeted. | [optional]
**country_code** | Option<**String**> | ISO-3166 alpha-2 of the country a sub-country geo result (city, region, zip, metro) belongs to, when the platform reports it (Meta does). Useful to know whether a location falls under the EU DSA disclosure rules before creating the ad. | [optional]
**platform_id** | Option<**String**> | Only on `country` results: the platform's own id for the country, which `id` replaced with the ISO code (TikTok's native location_id, a GeoNames id such as 2635167 for GB; Meta's country key; Google's geo target constant id; X's targeting value; LinkedIn's geo URN). Use it to match a country against what the platform reports back, e.g. `location_ids` in a TikTok `nativeSettings` read. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


