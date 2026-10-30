# CampaignSubmission

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**campaign_id** | **String** |  | 
**participant_id** | **String** |  | 
**creator_id** | **String** |  | 
**account_id** | **String** | The creator account the post was published from. | 
**platform** | **Platform** |  (enum: tiktok, instagram, youtube, threads, pinterest, facebook, twitter) | 
**platform_post_id** | **String** |  | 
**platform_post_url** | Option<**String**> |  | 
**external_post_id** | Option<**String**> | The tracked external post (see /v1/external-posts). | 
**tracking_window_id** | Option<**String**> |  | 
**media_hash** | Option<**String**> |  | 
**submitted_at** | **String** |  | 
**post_published_at** | Option<**String**> |  | 
**status** | **Status** |  (enum: received, tracking, pending_review, approved, rejected, expired, withdrawn) | 
**reject_reason** | Option<**String**> |  | 
**review_round** | **i32** | How many times the post was reopened after a reject. 0 until the first reopen. | 
**reviewed_by** | Option<**String**> | User id of the reviewer. | 
**reviewed_at** | Option<**String**> |  | 
**views_at_submission** | Option<**i32**> | Views when the post was submitted. They count toward earnings like every later view. | 
**views_latest** | Option<**i32**> | Latest view count read for the post, frozen at the tracking window end. | 
**views_eligible** | Option<**i32**> | Views that count toward earnings: every view the platform reports for the post, including those before submission, read at the tracking window end at the latest: once the window completes or is cancelled, the last read at or before its end is final and this value stops moving. | 
**engagements_latest** | Option<**i32**> | The campaign engagement types summed at the latest read (all four on a views campaign), frozen at the tracking window end like `viewsEligible`. An `engagements` campaign earns on this count. | 
**last_accrued_views** | **i32** |  | 
**accrued_cents** | **i32** |  | 
**approved_cents** | **i32** |  | 
**authenticity_score** | Option<**i32**> |  | 
**authenticity_confidence** | Option<**f64**> |  | 
**flags** | [**Vec<models::CampaignSubmissionFlag>**](CampaignSubmissionFlag.md) |  | 
**created_at** | **String** |  | 
**updated_at** | **String** |  | 
**creator** | [**models::WebhookPayloadCampaignSubmissionCreator**](WebhookPayloadCampaignSubmissionCreator.md) |  | 
**authenticity** | [**models::CampaignSubmissionAuthenticity**](CampaignSubmissionAuthenticity.md) |  | 
**earned_cents** | **i32** | approvedCents once approved, otherwise accruedCents. | 
**released_cents** | **i32** | Approved cents whose hold is over, so payable or already paid out. 0 unless approved. | 
**paid_out_cents** | **i32** | What rejecting this post could not take back now: releasedCents beyond the creator's payable balance. It stays paid; the dashboard warns before such a reject. | 
**window** | [**models::CampaignSubmissionWindow**](CampaignSubmissionWindow.md) |  | 
**post** | [**models::CampaignSubmissionPost**](CampaignSubmissionPost.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


