# CreatorPortalCampaign

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | The campaign id, as in a link-recovery URL. | 
**name** | **String** |  | 
**brand_name** | **String** |  | 
**logo_url** | Option<**String**> |  | 
**theme** | Option<**serde_json::Value**> | Same keys as the `welcomeTheme` parameter of `GET /v1/connect/{platform}`. | 
**status** | **Status** |  (enum: draft, active, paused, closed) | 
**platforms** | **Vec<String>** |  | 
**content_rules** | Option<**String**> |  | 
**starts_at** | Option<**String**> |  | 
**ends_at** | Option<**String**> |  | 
**started_at** | **String** | Posts published before this moment do not count: `startsAt`, else when the campaign went live. | 
**currency** | **String** |  | 
**economics** | [**models::CreatorPortalEconomics**](CreatorPortalEconomics.md) |  | 
**max_post_age_minutes** | Option<**i32**> | A post must be submitted within this many minutes of publishing. Null means any age. Either way, only posts published after the campaign started are accepted. | 
**hold_days** | **i32** | Days approved earnings stay owed before they become payable. | 
**tracking_days** | **i32** | Days each submitted post is tracked for views. | 
**max_accounts_per_participant** | Option<**i32**> | How many connected accounts can submit posts. Null means no limit. | 
**join_approval** | **JoinApproval** | manual: a creator who joins through the open link waits `pending` until the campaign team accepts them. (enum: auto, manual) | 
**require_draft_approval** | **bool** | The creator uploads a draft for review first, and submits the live post for an approved draft. | 
**sample_products** | [**Vec<models::CreatorCampaignSampleProduct>**](CreatorCampaignSampleProduct.md) | Products the creator can ask a free sample of; empty when the campaign offers none. | 
**sample_content_due_days** | **i32** | Days after a sample is approved by which a post is expected. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


