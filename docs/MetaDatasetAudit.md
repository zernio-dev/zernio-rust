# MetaDatasetAudit

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** |  | 
**ad_account_id** | **String** |  | 
**dataset** | Option<[**models::MetaDatasetAuditDataset**](MetaDatasetAuditDataset.md)> |  | 
**datasets** | [**Vec<models::MetaDatasetAuditDatasetsInner>**](MetaDatasetAuditDatasetsInner.md) | Every pixel assigned to the ad account. | 
**window** | [**models::MetaDatasetAuditWindow**](MetaDatasetAuditWindow.md) |  | 
**events** | [**Vec<models::MetaDatasetAuditEventsInner>**](MetaDatasetAuditEventsInner.md) | One entry per event Meta counted in the window or scored, busiest first. | 
**findings** | [**Vec<models::MetaDatasetAuditFindingsInner>**](MetaDatasetAuditFindingsInner.md) | Problems the numbers show, most damaging first. | 
**unavailable** | [**Vec<models::MetaDatasetAuditUnavailableInner>**](MetaDatasetAuditUnavailableInner.md) | What the audit could not read, and why. | 
**checked_at** | **String** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


