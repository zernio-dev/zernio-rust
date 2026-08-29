# AttachCampaignAssetsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Zernio Google Ads SocialAccount id — resolves the customer id + refresh token. | 
**customer_id** | Option<**String**> | Numeric Google Ads customer id. Required when the connection has multiple Google Ads accounts; optional (and inferred) when it has only one. | [optional]
**sitelinks** | Option<[**Vec<models::AttachCampaignAssetsRequestSitelinksInner>**](AttachCampaignAssetsRequestSitelinksInner.md)> | See POST /v1/ads/create sitelinks — same shape. | [optional]
**callouts** | Option<**Vec<String>**> |  | [optional]
**structured_snippets** | Option<[**Vec<models::AttachCampaignAssetsRequestStructuredSnippetsInner>**](AttachCampaignAssetsRequestStructuredSnippetsInner.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


