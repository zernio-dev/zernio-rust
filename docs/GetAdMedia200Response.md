# GetAdMedia200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ad_id** | Option<**String**> |  | [optional]
**platform** | Option<**String**> | 'facebook' or 'instagram'. Only Meta is supported for now. | [optional]
**synced** | Option<**bool**> | False when the ad was read live from Meta because it is not in Zernio's store (request made with `accountId`). | [optional]
**media** | Option<[**Vec<models::GetAdMedia200ResponseMediaInner>**](GetAdMedia200ResponseMediaInner.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


