# TikTokAdsPlatformQueryBody

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio id of the connected TikTok ads account. | 
**ad_account_id** | **String** | The numeric TikTok advertiser id. | 
**report_type** | Option<**ReportType**> | Defaults to BASIC. (enum: BASIC, AUDIENCE) | [optional][default to Basic]
**data_level** | **DataLevel** | The level of each row. (enum: AUCTION_ADVERTISER, AUCTION_CAMPAIGN, AUCTION_ADGROUP, AUCTION_AD) | 
**dimensions** | **Vec<String>** | TikTok dimensions, 1 to 4. | 
**metrics** | **Vec<String>** | TikTok metrics, up to 100. | 
**filtering** | Option<[**Vec<models::MetaAdsPlatformQueryBodyFilteringInner>**](MetaAdsPlatformQueryBodyFilteringInner.md)> | TikTok filters of field, operator and value, up to 25. A filter on an entity finer than dataLevel is refused. | [optional]
**from_date** | [**String**](String.md) | First day, YYYY-MM-DD, inclusive. | 
**to_date** | [**String**](String.md) | Last day, YYYY-MM-DD, inclusive. | 
**page_size** | Option<**i32**> | Rows per page, up to 1,000. Defaults to 1,000. | [optional][default to 1000]
**cursor** | Option<**String**> | The pagination.nextCursor of the previous page, unchanged. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


