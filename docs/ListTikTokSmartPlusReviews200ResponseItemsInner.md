# ListTikTokSmartPlusReviews200ResponseItemsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**smart_plus_ad_id** | Option<**String**> |  | [optional]
**ad_group_id** | Option<**String**> |  | [optional]
**campaign_id** | Option<**String**> |  | [optional]
**review** | Option<[**models::TikTokSmartPlusAdLevelReview**](TikTokSmartPlusAdLevelReview.md)> |  | [optional]
**materials** | Option<[**Vec<models::TikTokSmartPlusMaterialReview>**](TikTokSmartPlusMaterialReview.md)> | One entry per creative TikTok reviewed (`material_review_infos`). | [optional]
**read_at** | Option<**String**> | When the verdict was read from TikTok, kept as is when served from the store. Older than `maxAgeSeconds` means stale. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


