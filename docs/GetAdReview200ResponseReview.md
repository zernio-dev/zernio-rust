# GetAdReview200ResponseReview

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**approved** | Option<**bool**> | TikTok `is_approved`. | [optional]
**review_status** | Option<**String**> | TikTok `review_status`, verbatim: ALL_AVAILABLE (approved everywhere), PART_AVAILABLE (approved for part of the targeting), UNAVAILABLE (rejected). | [optional]
**forbidden_placements** | Option<**Vec<String>**> |  | [optional]
**forbidden_ages** | Option<**Vec<String>**> |  | [optional]
**forbidden_locations** | Option<**Vec<String>**> |  | [optional]
**forbidden_operating_systems** | Option<**Vec<String>**> |  | [optional]
**rejections** | Option<[**Vec<models::GetAdReview200ResponseReviewRejectionsInner>**](GetAdReview200ResponseReviewRejectionsInner.md)> | One entry per rejected piece of content (TikTok `reject_info`). Empty when the ad was approved. | [optional]
**read_at** | Option<**String**> | When the verdict was read from TikTok. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


