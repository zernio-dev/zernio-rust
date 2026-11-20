# GoogleAdsPlatformQueryBody

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio id of the connected Google Ads account. | 
**ad_account_id** | Option<**String**> | The Google Ads customer to query. Defaults to the connection's own customer. | [optional]
**query** | **String** | A GAQL SELECT statement, up to 10,000 characters. Read only. | 
**cursor** | Option<**String**> | The pagination.nextCursor of the previous page, unchanged. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


