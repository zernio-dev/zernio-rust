# CreateCommentAutomationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** |  | 
**account_id** | **String** | Instagram or Facebook account ID | 
**platform_post_id** | Option<**String**> | Platform media/post ID. Omit for an account-wide (any-post) automation. | [optional]
**post_id** | Option<**String**> | Zernio post ID. Required only when also targeting a specific post via platformPostId. | [optional]
**post_title** | Option<**String**> | Post content snippet for display | [optional]
**name** | **String** | Automation label | 
**keywords** | Option<**Vec<String>**> | Trigger keywords (empty = any comment triggers) | [optional]
**match_mode** | Option<**MatchMode**> |  (enum: exact, contains) | [optional][default to Contains]
**dm_message** | **String** | DM text to send to commenter. Max 640 chars when buttons are set, otherwise ~1000. | 
**buttons** | Option<[**Vec<models::DmButton>**](DmButton.md)> | Optional inline DM buttons (1-3). Phone buttons are Facebook-only. Omit or pass [] for a plain-text DM. | [optional]
**comment_reply** | Option<**String**> | Optional public reply to the comment | [optional]
**link_tracking** | Option<**bool**> | Wrap link buttons in the DM in a tracked redirect so clicks are counted (Link Clicks / CTR). Pass false to send links exactly as written. Defaults to on. | [optional][default to true]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


