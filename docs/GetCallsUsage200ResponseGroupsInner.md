# GetCallsUsage200ResponseGroupsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | Option<**String**> | The group key: a `YYYY-MM-DD` UTC day, one of your numbers, a channel, or a profile id. | [optional]
**profile_id** | Option<**String**> | With `groupBy=profile` only: the profile id (same as `key`). | [optional]
**external_id** | Option<**String**> | With `groupBy=profile` only: the externalId set on the profile, null when it has none. | [optional]
**calls** | Option<**i32**> |  | [optional]
**answered** | Option<**i32**> |  | [optional]
**minutes** | Option<**f64**> |  | [optional]
**billable_usd** | Option<**f64**> |  | [optional]
**meta_usd** | Option<**f64**> |  | [optional]
**branded_calls** | Option<**i32**> |  | [optional]
**branded_call_usd** | Option<**f64**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


