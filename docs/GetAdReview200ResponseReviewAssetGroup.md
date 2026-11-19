# GetAdReview200ResponseReviewAssetGroup

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**primary_status** | Option<**String**> | asset_group.primary_status, verbatim: ELIGIBLE, LIMITED, NOT_ELIGIBLE, PAUSED, PENDING, REMOVED. | 
**primary_status_reasons** | **Vec<String>** | asset_group.primary_status_reasons, verbatim, such as ASSET_GROUP_DISAPPROVED, ASSET_GROUP_UNDER_REVIEW, ASSET_GROUP_LIMITED, CAMPAIGN_PAUSED. Empty when the group serves without issues. | 
**assets** | [**Vec<models::GetAdReview200ResponseReviewAssetGroupAssetsInner>**](GetAdReview200ResponseReviewAssetGroupAssetsInner.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


