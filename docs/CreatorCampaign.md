# CreatorCampaign

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**user_id** | **String** | The workspace billing owner the campaign belongs to. | 
**profile_id** | **String** | The profile that scopes the campaign: API keys, teammates and webhooks scoped to it reach the campaign. | 
**kind** | **String** |  | 
**name** | **String** |  | 
**brand_name** | **String** |  | 
**status** | **Status** | draft until activated; active accepts submissions and accrues; paused stops new submissions; closed is final. (enum: draft, active, paused, closed) | 
**r#type** | **Type** | Same as economics.type. (enum: cpm, per_post, pool) | 
**currency** | **String** |  | 
**platforms** | **Vec<Platforms>** |  (enum: tiktok, instagram, youtube, threads, pinterest, facebook, twitter) | 
**content_rules** | Option<**String**> | Free-text rules shown to creators on the join page. | 
**starts_at** | Option<**String**> |  | 
**ends_at** | Option<**String**> | No new submissions after this time; the campaign closes once every tracking window had its final read. | 
**tracking_days** | **i32** | How long each submitted post is tracked. | 
**hold_days** | **i32** | Days approved earnings are held before they become payable. | 
**max_post_age_minutes** | Option<**i32**> | A post older than this many minutes when submitted is refused. Null (the default) accepts any age. Either way, a post published before the campaign started (`startsAt`, or `activatedAt` without one) is refused. | 
**activated_at** | Option<**String**> | When the campaign was first activated. Without `startsAt`, posts must be published after this moment. | 
**settlement** | **Settlement** | none: settle records a payout made elsewhere. external: you pay from your own rails on campaign_payout.payable and settle with your reference. treasury: settle moves the money from your Zernio balance to the creator's Stripe account, and the creator sets up payouts from their campaign page. (enum: none, external, treasury) | 
**economics** | [**models::CreatorCampaignEconomics**](CreatorCampaignEconomics.md) |  | 
**caps** | [**models::CreatorCampaignCaps**](CreatorCampaignCaps.md) |  | 
**branding** | Option<[**models::CreatorCampaignBranding**](CreatorCampaignBranding.md)> |  | 
**budget_exhausted_at** | Option<**String**> |  | 
**closed_at** | Option<**String**> |  | 
**payable_scanned_at** | Option<**String**> | Internal watermark of the payable scan. | 
**created_at** | **String** |  | 
**updated_at** | **String** |  | 
**has_open_invite** | **bool** | True once an open invite link was created. The link itself is returned only when it is created. | 
**consumed_cents** | **i32** | Budget used so far: earnings accrued, approved or adjusted against the campaign. | 
**participant_count** | **i32** |  | 
**submission_counts** | [**models::CampaignSubmissionCounts**](CampaignSubmissionCounts.md) |  | 
**payable_cents** | **i32** | What the campaign's creators can be paid now, summed over every participant's payable balance. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


