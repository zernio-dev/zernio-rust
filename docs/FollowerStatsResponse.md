# FollowerStatsResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**accounts** | Option<[**Vec<models::AccountWithFollowerStats>**](AccountWithFollowerStats.md)> |  | [optional]
**stats** | Option<[**std::collections::HashMap<String, Vec<models::FollowerStatsResponseStatsValueInner>>**](Vec.md)> |  | [optional]
**date_range** | Option<[**models::FollowerStatsResponseDateRange**](FollowerStatsResponseDateRange.md)> |  | [optional]
**granularity** | Option<**String**> |  | [optional]
**pagination** | Option<[**models::AccountCursorPagination**](AccountCursorPagination.md)> | Present when limit or cursor is sent, and on the default page of 25 that an API request without accountIds gets. | [optional]
**warning** | Option<**String**> | Only when the response was cut: the default page of 25 accounts (page through the rest with cursor), or a date range longer than a year (dateRange.from shows where the data starts). Both reasons are joined when they apply together. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


