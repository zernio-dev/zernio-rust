# GetCampaignTargeting200ResponseLocationsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**geo_target_id** | Option<**String**> | Numeric id from Google's geoTargetConstants/{id}. | [optional]
**negative** | Option<**bool**> | true = excluded location. | [optional]
**name** | Option<**String**> | Google's geo_target_constant.name, e.g. \"United States\"; null when the id could not be resolved. | [optional]
**canonical_name** | Option<**String**> | Google's geo_target_constant.canonical_name, e.g. \"California, United States\"; null when the id could not be resolved. | [optional]
**r#type** | Option<**String**> | Google's geo_target_constant.target_type, e.g. \"Country\", \"Region\", \"City\"; null when the id could not be resolved. | [optional]
**country_code** | Option<**String**> | Google's geo_target_constant.country_code, an ISO 3166-1 alpha-2 code; null when the id could not be resolved. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


