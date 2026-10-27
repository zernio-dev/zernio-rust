# GetAdSetTargeting200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ad_set_id** | Option<**String**> |  | [optional]
**targeting** | Option<[**models::TargetingSpec**](TargetingSpec.md)> | Only the keys the ad group sets. `regions`, `metros`, `cities` and `zips` entries carry `{ key, name }`; `interests` carry `{ id, name }`. | [optional]
**start_date** | Option<**String**> | The ad group's start_time, null when it has none. | [optional]
**end_date** | Option<**String**> | The ad group's end_time, null when it runs continuously. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


