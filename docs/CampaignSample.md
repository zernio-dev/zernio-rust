# CampaignSample

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**campaign_id** | **String** |  | 
**participant_id** | **String** |  | 
**creator** | [**models::CreatorCampaignAdResultsSubmissionsInnerCreator**](CreatorCampaignAdResultsSubmissionsInnerCreator.md) |  | 
**store_account_id** | **String** | The store the sample comes from. | 
**product_id** | **String** |  | 
**variant_id** | Option<**String**> |  | 
**product_title** | **String** |  | 
**variant_title** | Option<**String**> |  | 
**shipping_address** | [**models::CampaignSampleShippingAddress**](CampaignSampleShippingAddress.md) |  | 
**note** | Option<**String**> | The creator's note. | 
**status** | **Status** | pending: waits for review. approved: a discount code was created. shipped: you recorded that you sent it. declined: final for this request. (enum: pending, approved, shipped, declined) | 
**decline_reason** | Option<**String**> |  | 
**discount_code** | Option<**String**> | The 100%-off, single-use code for the product, set on approval. | 
**tracking_url** | Option<**String**> |  | 
**approved_at** | Option<**String**> |  | 
**shipped_at** | Option<**String**> |  | 
**requested_at** | **String** |  | 
**content_due_at** | Option<**String**> | When a post is due: the approval plus the campaign's `sampleContentDueDays`. Null unless approved or shipped. | 
**content_owed** | **bool** | True past `contentDueAt` when the creator submitted no post since the approval. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


