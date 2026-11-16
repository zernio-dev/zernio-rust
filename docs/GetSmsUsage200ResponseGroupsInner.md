# GetSmsUsage200ResponseGroupsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | Option<**String**> | A `YYYY-MM-DD` UTC day, one of your numbers, or a profile id. | [optional]
**profile_id** | Option<**String**> | With `groupBy=profile` only: the profile id (same as `key`). | [optional]
**external_id** | Option<**String**> | With `groupBy=profile` only: the externalId set on the profile, null when it has none. | [optional]
**sent** | Option<**i32**> |  | [optional]
**received** | Option<**i32**> |  | [optional]
**total** | Option<**i32**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


