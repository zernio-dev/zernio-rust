# FollowerStatsResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**accounts** | Option<[**Vec<models::AccountWithFollowerStats>**](AccountWithFollowerStats.md)> |  | [optional]
**stats** | Option<[**std::collections::HashMap<String, Vec<models::FollowerStatsResponseStatsValueInner>>**](Vec.md)> |  | [optional]
**date_range** | Option<[**models::FollowerStatsResponseDateRange**](FollowerStatsResponseDateRange.md)> |  | [optional]
**granularity** | Option<**String**> |  | [optional]
**pagination** | Option<[**models::AccountCursorPagination**](AccountCursorPagination.md)> | Present when limit or cursor is sent, and on the default page of 25 that an API request without accountIds gets. | [optional]
**warning** | Option<**String**> | Only when the default page of 25 cut the list. Page through the rest with cursor. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


