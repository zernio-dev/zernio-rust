# CreateCommentAutomationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** |  | 
**account_id** | **String** | Instagram or Facebook account ID | 
**trigger** | Option<**Trigger**> | What fires the automation. 'comment' (keyword comment on a post) or 'story_reply' (keyword reply to an Instagram story). For 'story_reply', platformPostId is the story media id (omit for any story). (enum: comment, story_reply) | [optional][default to Comment]
**platform_post_id** | Option<**String**> | Platform media/post ID (or story media id when trigger=story_reply). Omit for an account-wide (any-post / any-story) automation. | [optional]
**post_id** | Option<**String**> | Zernio post ID. Required only when also targeting a specific post via platformPostId. | [optional]
**post_title** | Option<**String**> | Post content snippet for display | [optional]
**name** | **String** | Automation label | 
**keywords** | Option<**Vec<String>**> | Trigger keywords (empty = any comment triggers) | [optional]
**match_mode** | Option<**MatchMode**> |  (enum: exact, contains) | [optional][default to Contains]
**dm_message** | **String** | DM text to send to commenter. Max 640 chars when buttons are set, otherwise ~1000. | 
**buttons** | Option<[**Vec<models::DmButton>**](DmButton.md)> | Optional inline DM buttons (1-3). Phone buttons are Facebook-only. Omit or pass [] for a plain-text DM. | [optional]
**comment_reply** | Option<**String**> | Optional public reply to the comment | [optional]
**dm_message_variations** | Option<**Vec<String>**> | Optional alternate DM texts for random rotation. When set, each triggered comment sends one picked at random from [dmMessage, ...dmMessageVariations], so repeat commenters get slightly different DMs (helps avoid identical-message patterns). Up to 5. Buttons are attached to whichever text is picked, not varied. | [optional]
**comment_reply_variations** | Option<**Vec<String>**> | Optional alternate public replies, rotated at random alongside commentReply (picked independently of the DM). Up to 5. | [optional]
**link_tracking** | Option<**bool**> | Wrap link buttons in the DM in a tracked redirect so clicks are counted (Link Clicks / CTR). Pass false to send links exactly as written. Defaults to on. | [optional][default to true]
**click_tag** | Option<**String**> | Optional tag applied to a contact when they click a tracked link (requires linkTracking). Lets you segment clickers for broadcasts/sequences. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


