# ListAdGroupAssets200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ad_group_id** | Option<**String**> |  | [optional]
**sitelinks** | Option<[**Vec<models::ListAdGroupAssets200ResponseSitelinksInner>**](ListAdGroupAssets200ResponseSitelinksInner.md)> |  | [optional]
**callouts** | Option<[**Vec<models::ListAdGroupAssets200ResponseCalloutsInner>**](ListAdGroupAssets200ResponseCalloutsInner.md)> |  | [optional]
**structured_snippets** | Option<[**Vec<models::ListAdGroupAssets200ResponseStructuredSnippetsInner>**](ListAdGroupAssets200ResponseStructuredSnippetsInner.md)> |  | [optional]
**cached_at** | Option<**String**> | Time of the cached Google read. Null when no cache was used. | [optional]
**stale** | Option<**bool**> | True when exhausted quota required returning the last successful read. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


