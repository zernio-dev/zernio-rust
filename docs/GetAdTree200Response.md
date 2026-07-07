# GetAdTree200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**campaigns** | Option<[**Vec<models::AdTreeCampaign>**](AdTreeCampaign.md)> |  | [optional]
**backfill_pending** | Option<**bool**> | Present and true only on `202` responses: part of the requested date range is still being backfilled from the platform in the background. Retry the same request shortly; it returns 200 once the range is fully ingested. | [optional]
**pagination** | Option<[**models::Pagination**](Pagination.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


