# CampaignSubmissionDetail

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
**platform_post_url** | **String** |  | 
**external_post_id** | **String** | The tracked external post (see /v1/external-posts). | 
**tracking_window_id** | **String** |  | 
**media_hash** | **String** |  | 
**submitted_at** | **String** |  | 
**post_published_at** | **String** |  | 
**status** | **Status** |  (enum: received, tracking, pending_review, approved, rejected, expired, withdrawn) | 
**reject_reason** | **String** |  | 
**review_round** | **i32** | How many times the post was reopened after a reject. 0 until the first reopen. | 
**reviewed_by** | **String** | User id of the reviewer. | 
**reviewed_at** | **String** |  | 
**views_at_submission** | **i32** | Views when the post was submitted. They count toward earnings like every later view. | 
**views_latest** | **i32** | Latest view count read for the post, frozen at the tracking window end. | 
**views_eligible** | **i32** | Views that count toward earnings: every view the platform reports for the post, including those before submission, read at the tracking window end at the latest: once the window completes or is cancelled, the last read at or before its end is final and this value stops moving. | 
**engagements_latest** | **i32** | The campaign engagement types summed at the latest read (all four on a views campaign), frozen at the tracking window end like `viewsEligible`. An `engagements` campaign earns on this count. | 
**views_paid** | **i32** | Views from ads the creator ran: YouTube views from the advertising traffic source, X impressions beyond the organic ones. Null on other platforms and before the first read. On an organic-only campaign `viewsEligible` is the latest views minus these. | 
**paid_views_read_at** | **String** | When `viewsPaid` was last read. YouTube refreshes every 6 hours and reports ad views up to 2 days late; X about once a day while the post is under 30 days old. | 
**last_accrued_views** | **i32** |  | 
**accrued_cents** | **i32** |  | 
**approved_cents** | **i32** |  | 
**authenticity_score** | **i32** |  | 
**authenticity_confidence** | **f64** |  | 
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
**samples** | [**Vec<models::CampaignSubmissionDetailAllOfSamples>**](CampaignSubmissionDetailAllOfSamples.md) | Counters per sync, newest first, up to 500. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


