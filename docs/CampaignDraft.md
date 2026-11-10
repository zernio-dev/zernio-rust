# CampaignDraft

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**campaign_id** | **String** |  | 
**participant_id** | **String** |  | 
**creator** | [**models::CreatorCampaignAdResultsSubmissionsInnerCreator**](CreatorCampaignAdResultsSubmissionsInnerCreator.md) |  | 
**chain_id** | **String** | The id of the first version of the chain. | 
**version** | **i32** |  | 
**revision_of** | Option<**String**> | The version this one answers; null on version 1. | 
**media_url** | **String** |  | 
**media_type** | **MediaType** |  (enum: video, image) | 
**caption** | **String** |  | 
**status** | **Status** | submitted: waits for review. approved: the creator may publish it. revision_requested: the creator should upload a new version. rejected: final. (enum: submitted, approved, revision_requested, rejected) | 
**review_note** | Option<**String**> | The note sent with a revision request, or the rejection reason. | 
**reviewed_at** | Option<**String**> |  | 
**submitted_at** | **String** |  | 
**comments** | [**Vec<models::CampaignDraftCommentsInner>**](CampaignDraftCommentsInner.md) | Review comments on this version, in video order. | 
**submission_id** | Option<**String**> | The live post submitted for this draft, once the creator published it. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


