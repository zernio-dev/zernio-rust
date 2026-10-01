# SelectInstagramAccount200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | Option<**String**> |  | [optional]
**redirect_url** | Option<**String**> | Redirect URL if a custom redirect_url was provided. On an ads connect it also carries `adsAccountId`. | [optional]
**ads_account_id** | Option<**String**> | Ads connect only (the redirect_url carries adsConnect=true, as it does after GET /v1/connect/{platform}/ads). The metaads SocialAccount ID to use with the /v1/ads endpoints. `account.accountId` is the Instagram posting account. Absent when the ads account could not be created. | [optional]
**account** | Option<[**models::SelectInstagramAccount200ResponseAccount**](SelectInstagramAccount200ResponseAccount.md)> |  | [optional]
**accounts** | Option<**Vec<serde_json::Value>**> | pageIds only. The connected accounts, same shape as `account`. The redirect_url then carries `accountIds` (comma-separated) and `accountId` of the first. | [optional]
**failed** | Option<[**Vec<models::SelectFacebookPage200ResponseFailedInner>**](SelectFacebookPage200ResponseFailedInner.md)> | pageIds only. The Pages whose Instagram account could not be connected while the others were. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


