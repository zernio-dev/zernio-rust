# AnalyticsDashboardFollowers

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**current** | Option<**i32**> | Live follower count when the window includes today, otherwise the count the window ended on. | [optional]
**gained** | Option<**i32**> | Last minus first follower snapshot inside the window. Can be negative. | [optional]
**by_account** | Option<[**Vec<models::AnalyticsDashboardFollowersByAccountInner>**](AnalyticsDashboardFollowersByAccountInner.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


