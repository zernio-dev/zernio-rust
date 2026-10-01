# GetAnalyticsDashboard200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**date_range** | [**models::GetAnalyticsDashboard200ResponseDateRange**](GetAnalyticsDashboard200ResponseDateRange.md) |  | 
**totals** | [**models::AnalyticsDashboardTotals**](AnalyticsDashboardTotals.md) |  | 
**previous_totals** | Option<[**models::AnalyticsDashboardTotals**](AnalyticsDashboardTotals.md)> |  | [optional]
**followers** | [**models::AnalyticsDashboardFollowers**](AnalyticsDashboardFollowers.md) |  | 
**previous_followers** | Option<[**models::AnalyticsDashboardFollowers**](AnalyticsDashboardFollowers.md)> |  | [optional]
**daily** | [**Vec<models::GetAnalyticsDashboard200ResponseDailyInner>**](GetAnalyticsDashboard200ResponseDailyInner.md) | One entry per day of the window, days without data included as zeros. | 
**top_posts** | [**Vec<models::AnalyticsDashboardPost>**](AnalyticsDashboardPost.md) |  | 
**recent_posts** | [**Vec<models::AnalyticsDashboardPost>**](AnalyticsDashboardPost.md) |  | 
**data_as_of** | Option<**String**> | When the most recently synced account in scope was last synced. Null if none has synced yet. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


