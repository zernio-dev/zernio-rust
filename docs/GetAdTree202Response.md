# GetAdTree202Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**campaigns** | Option<[**Vec<models::AdTreeCampaign>**](AdTreeCampaign.md)> |  | [optional]
**pagination** | Option<[**models::Pagination**](Pagination.md)> |  | [optional]
**synced_at** | Option<**String**> | When the most recently synced ad on this page was last read from the platform. Null before the first sync. | [optional]
**previous_range** | Option<[**models::AdTreeResponsePreviousRange**](AdTreeResponsePreviousRange.md)> |  | [optional]
**backfill_pending** | **bool** | Always true on this response. Part of the requested range is still being backfilled; retry until the request returns 200. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


