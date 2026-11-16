# UsageAttributionGroup

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**by_product** | Option<[**models::UsageAttributionSliceByProduct**](UsageAttributionSliceByProduct.md)> |  | [optional]
**total_usd** | Option<**f64**> |  | [optional]
**key** | **String** | Profile id or account id, per `groupBy`. | 
**profile_id** | Option<**String**> | With `groupBy=profile` only: the profile id (same as `key`). | [optional]
**external_id** | Option<**String**> | With `groupBy=profile` only: the externalId set on the profile, null when it has none. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


