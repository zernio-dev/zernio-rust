# WebhookPayloadCampaignDraftDraft

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**chain_id** | **String** |  | 
**version** | **i32** |  | 
**revision_of** | Option<**String**> |  | 
**status** | **Status** |  (enum: submitted, approved, revision_requested, rejected) | 
**media_url** | **String** |  | 
**media_type** | **MediaType** |  (enum: video, image) | 
**caption** | **String** |  | 
**review_note** | Option<**String**> | The revision note or the rejection reason. | 
**comments** | [**Vec<models::CreatorPortalDraftCommentsInner>**](CreatorPortalDraftCommentsInner.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


