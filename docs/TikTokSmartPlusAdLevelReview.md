# TikTokSmartPlusAdLevelReview

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**review_status** | Option<[**models::TikTokSmartPlusReviewStatus**](TikTokSmartPlusReviewStatus.md)> |  | [optional]
**raw_review_status** | Option<**String**> | TikTok `review_status`, verbatim. | [optional]
**reject_reasons** | Option<**Vec<String>**> | Every distinct reason across `rejections`. | [optional]
**passed_locations** | Option<**Vec<String>**> | Location codes that passed the review. | [optional]
**appeal_status** | Option<**String**> | TikTok `appeal_status`, verbatim: NOT_APPEALED, APPEALING, APPEAL_SUCCESSFUL, APPEAL_FAILED, APPEAL_DONE. | [optional]
**appeal_reject_reasons** | Option<**Vec<String>**> |  | [optional]
**rejections** | Option<[**Vec<models::TikTokReviewRejection>**](TikTokReviewRejection.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


