# CreatorPortalDraft

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Pass as `draftId` when submitting the live post of an approved draft, or as `revisionOf` to answer a revision request. | 
**chain_id** | **String** |  | 
**version** | **i32** |  | 
**revision_of** | Option<**String**> |  | 
**status** | **Status** |  (enum: submitted, approved, revision_requested, rejected) | 
**media_url** | **String** |  | 
**media_type** | **MediaType** |  (enum: video, image) | 
**caption** | **String** |  | 
**review_note** | Option<**String**> |  | 
**comments** | [**Vec<models::CreatorPortalDraftCommentsInner>**](CreatorPortalDraftCommentsInner.md) |  | 
**submitted_at** | **String** |  | 
**reviewed_at** | Option<**String**> |  | 
**submission_id** | Option<**String**> | The live post submitted for this draft. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


