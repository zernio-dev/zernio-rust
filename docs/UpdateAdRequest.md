# UpdateAdRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | Option<**Status**> |  (enum: active, paused) | [optional]
**budget** | Option<[**models::UpdateAdRequestBudget**](UpdateAdRequestBudget.md)> |  | [optional]
**targeting** | Option<[**models::UpdateAdRequestTargeting**](UpdateAdRequestTargeting.md)> |  | [optional]
**creative** | Option<[**models::UpdateAdRequestCreative**](UpdateAdRequestCreative.md)> |  | [optional]
**name** | Option<**String**> | Rename the ad. Now propagated to Meta (POST /{ad-id}); non-Meta platforms return 501. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


