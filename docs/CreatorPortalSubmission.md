# CreatorPortalSubmission

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**platform** | **String** |  | 
**post_id** | **String** |  | 
**url** | Option<**String**> |  | 
**status** | **Status** |  (enum: received, tracking, pending_review, approved, rejected, expired, withdrawn) | 
**submitted_at** | **String** |  | 
**published_at** | Option<**String**> |  | 
**views** | **i32** | Latest view count read for the post. | 
**engagements** | Option<**i32**> | The campaign engagement types summed at the latest read. Null until the post is read. | 
**views_from_ads** | Option<**i32**> | Views that came from ads the creator ran, on YouTube and X. Null where the platform does not report them or before the first read. | 
**earned_cents** | **i32** |  | 
**reject_reason** | Option<**String**> |  | 
**flags** | **Vec<Flags>** | Creator-safe flags only. Every other review flag shows as `under_review`. (enum: unreachable, post_deleted, duplicate_post, under_review) | 
**tracking_ends_at** | Option<**String**> |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


