# ListAds202Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ads** | Option<[**Vec<models::Ad>**](Ad.md)> |  | [optional]
**pagination** | Option<[**models::Pagination**](Pagination.md)> |  | [optional]
**backfill_pending** | **bool** | Always true on this response. Part of the requested range is still being backfilled; retry until the request returns 200. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


