# GetTikTokSmartPlusAdReview200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ad_id** | Option<**String**> |  | [optional]
**platform** | Option<**Platform**> |  (enum: tiktok) | [optional]
**platform_ad_id** | Option<**String**> |  | [optional]
**smart_plus_ad_id** | Option<**String**> | The TikTok Smart+ ad whose review this is. | [optional]
**review** | Option<[**models::TikTokSmartPlusAdLevelReview**](TikTokSmartPlusAdLevelReview.md)> |  | [optional]
**materials** | Option<[**Vec<models::TikTokSmartPlusMaterialReview>**](TikTokSmartPlusMaterialReview.md)> | One entry per creative TikTok reviewed (`material_review_infos`). | [optional]
**read_at** | Option<**String**> | When the verdict was read from TikTok. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


