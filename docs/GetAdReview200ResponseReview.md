# GetAdReview200ResponseReview

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**approved** | Option<**bool**> | TikTok `is_approved`. Google and Meta: derived from the platform status (see the description). | [optional]
**review_status** | Option<**String**> | TikTok `review_status`, verbatim: ALL_AVAILABLE (approved everywhere), PART_AVAILABLE (approved for part of the targeting), UNAVAILABLE (rejected). Google: `review_status`. Meta: the ad's `effective_status`. | [optional]
**forbidden_placements** | Option<**Vec<String>**> |  | [optional]
**forbidden_ages** | Option<**Vec<String>**> |  | [optional]
**forbidden_locations** | Option<**Vec<String>**> |  | [optional]
**forbidden_operating_systems** | Option<**Vec<String>**> |  | [optional]
**rejections** | Option<[**Vec<models::GetAdReview200ResponseReviewRejectionsInner>**](GetAdReview200ResponseReviewRejectionsInner.md)> | One entry per rejected piece of content (TikTok `reject_info`). Empty when the ad was approved. | [optional]
**approval_status** | Option<**String**> | Google only. ad_group_ad.policy_summary.approval_status, verbatim. | [optional]
**policy_topics** | Option<[**Vec<models::GetAdReview200ResponseReviewPolicyTopicsInner>**](GetAdReview200ResponseReviewPolicyTopicsInner.md)> | Google only. ad_group_ad.policy_summary.policy_topic_entries. | [optional]
**review_feedback** | Option<[**models::GetAdReview200ResponseReviewReviewFeedback**](GetAdReview200ResponseReviewReviewFeedback.md)> |  | [optional]
**issues** | Option<**Vec<serde_json::Value>**> | Meta only. The Ad's `issues_info` objects (`error_code`, `error_message`, `error_summary`, `error_type`, `level`), verbatim. | [optional]
**read_at** | Option<**String**> | When the verdict was read from the platform. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


