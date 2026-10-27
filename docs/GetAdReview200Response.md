# GetAdReview200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ad_id** | Option<**String**> | Zernio ad id; null for an unsynced Meta ad read with `accountId`. | [optional]
**platform** | Option<**String**> |  | [optional]
**platform_ad_id** | Option<**String**> |  | [optional]
**synced** | Option<**bool**> | False when the ad was read live from Meta because it is not in Zernio's store. | [optional]
**review** | Option<[**models::GetAdReview200ResponseReview**](GetAdReview200ResponseReview.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


