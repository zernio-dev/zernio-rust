# ConversionAuditMonitor

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | The monitor id. | 
**host** | **String** | The watched host, lowercase and without `www.`. | 
**report_url** | **String** | The host's public report on is-bleeding.com. | 
**score** | Option<**i32**> | The score of the last check (0 to 100), or null before the first readable scan. | 
**grade** | Option<**String**> | The grade of the last check. | 
**score_history** | [**Vec<models::ConversionAuditMonitorScoreHistoryInner>**](ConversionAuditMonitorScoreHistoryInner.md) | The score of each of the last 30 checks, oldest first. | 
**created_at** | **String** |  | 
**last_checked_at** | Option<**String**> |  | 
**next_check_at** | **String** | When the next daily check is due. | 
**last_alerted_at** | Option<**String**> | When the last alert email went out. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


