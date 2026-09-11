# UpdateAdRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**headlines** | Option<[**Vec<models::GoogleRsaHeadline>**](GoogleRsaHeadline.md)> | Google Search and Display only. Replaces the complete headline list. Search takes 3-15, Display 1-5 and rejects pinnedField; the count is checked once the ad's channel is known. No padding or truncation on update. | [optional]
**descriptions** | Option<[**Vec<models::GoogleRsaDescription>**](GoogleRsaDescription.md)> | Google Search and Display only. Replaces the complete description list. Search takes 2-4, Display 1-5 and rejects pinnedField. No padding or truncation on update. | [optional]
**final_urls** | Option<**Vec<String>**> | Google Search and Display only. Replaces final URLs. Omitted lists stay unchanged. For Performance Max use assetGroup.finalUrl. | [optional]
**asset_group** | Option<[**models::GooglePmaxAssetGroupUpdate**](GooglePmaxAssetGroupUpdate.md)> | Google Performance Max only. Replaces whole asset roles on the ad's asset group. Returns 422 on any other platform or channel. | [optional]
**status** | Option<**Status**> |  (enum: active, paused) | [optional]
**budget** | Option<[**models::UpdateAdRequestBudget**](UpdateAdRequestBudget.md)> |  | [optional]
**targeting** | Option<[**models::UpdateAdRequestTargeting**](UpdateAdRequestTargeting.md)> |  | [optional]
**creative** | Option<[**models::UpdateAdRequestCreative**](UpdateAdRequestCreative.md)> |  | [optional]
**name** | Option<**String**> | Rename the ad. Now propagated to Meta (POST /{ad-id}); non-Meta platforms return 501. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


