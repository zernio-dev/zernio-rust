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
**match_mode** | Option<**MatchMode**> | How a keyword is compared with the comment. 'contains' (default) matches anywhere, even inside another word (keyword 'app' fires on 'happy'). 'word' matches the keyword only as a standalone word. 'exact' requires the whole comment to be exactly the keyword. (enum: exact, contains, word) | [optional][default to Contains]
**exclude_keywords** | Option<**Vec<String>**> | Comments containing one of these never trigger the automation, even when a trigger keyword also matches. Compared using the same matchMode. | [optional]
**typo_tolerance** | Option<**bool**> | Only with matchMode=word: also fire on close misspellings of a keyword (one edit for 4-7 character keywords, two from 8 up). Keywords shorter than 4 characters are never fuzzy-matched. | [optional]
**dm_message** | **String** | DM text to send to commenter. Max 640 chars when buttons are set, otherwise ~1000. | 
**buttons** | Option<[**Vec<models::DmButton>**](DmButton.md)> | Optional inline DM buttons (1-3). Phone buttons are Facebook-only. Omit or pass [] for a plain-text DM. | [optional]
**template** | Option<[**models::CommentAutomationTemplate**](CommentAutomationTemplate.md)> | Optional product card sent INSTEAD of the plain dmMessage bubble. Mutually exclusive with buttons. dmMessage stays required: it is what gets sent the moment the card is cleared. | [optional]
**comment_reply** | Option<**String**> | Optional public reply to the comment | [optional]
**dm_message_variations** | Option<**Vec<String>**> | Optional alternate DM texts for random rotation. When set, each triggered comment sends one picked at random from [dmMessage, ...dmMessageVariations], so repeat commenters get slightly different DMs (helps avoid identical-message patterns). Up to 5. Buttons are attached to whichever text is picked, not varied. | [optional]
**comment_reply_variations** | Option<**Vec<String>**> | Optional alternate public replies, rotated at random alongside commentReply (picked independently of the DM). Up to 5. | [optional]
**link_tracking** | Option<**bool**> | Wrap link buttons in the DM in a tracked redirect so clicks are counted (Link Clicks / CTR). Pass false to send links exactly as written. Defaults to on. | [optional][default to true]
**click_tag** | Option<**String**> | Optional tag applied to a contact when they click a tracked link (requires linkTracking). Lets you segment clickers for broadcasts/sequences. | [optional]
**dm_delay_seconds** | Option<**i32**> | Seconds to wait after the trigger before sending the DM. Omit or send 0 to reply immediately (the default). Max 86400 (24h). The trigger is still matched and deduplicated the moment the comment arrives, so a delay only moves when the response is sent. | [optional]
**comment_reply_delay_seconds** | Option<**i32**> | Seconds to wait before posting the public comment reply. Omit or send 0 to post it right after the DM (the default). The reply never goes out before the DM, so a value below dmDelaySeconds is raised to it. Ignored when trigger=story_reply, which has no public reply. | [optional]
**also_match_in_dms** | Option<**bool**> | Also fire these keywords on a plain inbound DM, so the automation answers people who message the keyword instead of commenting it. Requires at least one keyword (an empty keyword list means 'match anything', which would answer every inbound message) and is rejected on story_reply automations, which already trigger on DMs. Dedup is per door: a contact who already received the DM from their comment can still receive it from a DM. | [optional][default to false]
**audience** | Option<[**models::CommentAutomationAudience**](CommentAutomationAudience.md)> |  | [optional]
**follow_gate** | Option<[**models::CommentAutomationFollowGate**](CommentAutomationFollowGate.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


