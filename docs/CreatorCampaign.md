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
**r#type** | **Type** | Same as economics.type. (enum: cpm, per_post, pool, retainer, commission, ad_performance) | 
**currency** | **String** |  | 
**platforms** | **Vec<Platforms>** |  (enum: tiktok, instagram, youtube, threads, pinterest, facebook, twitter) | 
**content_rules** | Option<**String**> | Free-text rules shown to creators on the join page. | 
**starts_at** | Option<**String**> |  | 
**ends_at** | Option<**String**> | No new submissions after this time; the campaign closes once every tracking window had its final read. | 
**tracking_days** | **i32** | How long each submitted post is tracked. | 
**hold_days** | **i32** | Days approved earnings are held before they become payable. | 
**max_post_age_minutes** | Option<**i32**> | A post older than this many minutes when submitted is refused. Null (the default) accepts any age. Either way, a post published before the campaign started (`startsAt`, or `activatedAt` without one) is refused. | 
**activated_at** | Option<**String**> | When the campaign was first activated. Without `startsAt`, posts must be published after this moment. | 
**settlement** | **Settlement** | none: settle records a payout made elsewhere. external: you pay from your own rails on campaign_payout.payable and settle with your reference. treasury: you pay by card with a payout batch and Zernio pays each creator in your name 7 days after the charge. (enum: none, external, treasury) | 
**economics** | [**models::CreatorCampaignEconomics**](CreatorCampaignEconomics.md) |  | 
**caps** | [**models::CreatorCampaignCaps**](CreatorCampaignCaps.md) |  | 
**branding** | Option<[**models::CreatorCampaignBranding**](CreatorCampaignBranding.md)> |  | 
**budget_exhausted_at** | Option<**String**> |  | 
**closed_at** | Option<**String**> |  | 
**payable_scanned_at** | Option<**String**> | Internal watermark of the payable scan. | 
**join_approval** | **JoinApproval** | auto: creators who join through the open link are active at once. manual: they land `pending` until you approve or deny them. Personal invites are never held. (enum: auto, manual) | 
**require_draft_approval** | **bool** | Creators upload a draft for review first, and submit the live post for an approved draft (`draftId`). | 
**store_account_id** | Option<**String**> | The connected store (Shopify or WooCommerce) whose orders pay commission and whose products creators can ask as samples. Null when the campaign has neither. | 
**sample_products** | [**Vec<models::CreatorCampaignSampleProduct>**](CreatorCampaignSampleProduct.md) | Products creators can ask a free sample of. | 
**sample_content_due_days** | **i32** | Days after a sample is approved before a creator with no post since shows as owing content (`contentOwed`). | 
**created_at** | **String** |  | 
**updated_at** | **String** |  | 
**has_open_invite** | **bool** | True once an open invite link was created. The link itself is returned only when it is created. | 
**consumed_cents** | **i32** | Budget used so far: earnings accrued, approved or adjusted against the campaign. | 
**participant_count** | **i32** |  | 
**submission_counts** | [**models::CampaignSubmissionCounts**](CampaignSubmissionCounts.md) |  | 
**payable_cents** | **i32** | What the campaign's creators can be paid now, summed over every participant's payable balance. | 
**landing_url** | Option<**String**> | The page creator tracking links open. | [optional]
**code_discount_percent** | Option<**i32**> | What each creator discount code takes off. | [optional]
**auto_payout** | Option<[**models::CreatorCampaignAutoPayout**](CreatorCampaignAutoPayout.md)> |  | [optional]
**pending_participant_count** | **i32** | Creators who asked to join through the open link and wait for a decision. Not counted in `participantCount`. | 
**draft_counts** | [**models::CampaignDraftCounts**](CampaignDraftCounts.md) |  | 
**sample_counts** | [**models::CampaignSampleCounts**](CampaignSampleCounts.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


