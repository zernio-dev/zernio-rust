# GetAdAccountHierarchy200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | Option<**String**> |  | [optional]
**roots** | Option<[**Vec<models::GetAdAccountHierarchy200ResponseRootsInner>**](GetAdAccountHierarchy200ResponseRootsInner.md)> |  | [optional]
**direct_customers** | Option<[**Vec<models::GetAdAccountHierarchy200ResponseDirectCustomersInner>**](GetAdAccountHierarchy200ResponseDirectCustomersInner.md)> |  | [optional]
**unavailable** | Option<[**Vec<models::GetAdAccountHierarchy200ResponseUnavailableInner>**](GetAdAccountHierarchy200ResponseUnavailableInner.md)> |  | [optional]
**truncated** | Option<**bool**> |  | [optional]
**cached_at** | Option<**String**> | When this data was fetched from Google. Null on a live read. | [optional]
**stale** | Option<**bool**> | True when Google's quota was exhausted and this is the last successful fetch. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


