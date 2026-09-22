# UpdateAccountSitelinksRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Zernio Google Ads connection id. | 
**ad_account_id** | Option<**String**> | Platform ad account ID (Google customer ID, digits only). Required when the connection has multiple customers. | [optional]
**customer_id** | Option<**String**> | Alias of adAccountId, kept for existing callers | [optional]
**updates** | [**Vec<models::UpdateAccountSitelinksRequestUpdatesInner>**](UpdateAccountSitelinksRequestUpdatesInner.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


