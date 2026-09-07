# GetAdsSearchTerms200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**customer_id** | Option<**String**> |  | [optional]
**data** | Option<[**Vec<models::GetAdsSearchTerms200ResponseDataInner>**](GetAdsSearchTerms200ResponseDataInner.md)> |  | [optional]
**paging** | Option<[**models::GetAdsSearchTerms200ResponsePaging**](GetAdsSearchTerms200ResponsePaging.md)> |  | [optional]
**cached_at** | Option<**String**> | When this data was fetched from Google. Null when it was never served from cache. | [optional]
**stale** | Option<**bool**> | True when Google's daily API quota was exhausted and this is the last successful fetch, not a live read. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


