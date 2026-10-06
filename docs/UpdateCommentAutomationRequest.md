# UpdateCommentAutomationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | Option<**String**> |  | [optional]
**trigger** | Option<**Trigger**> | What fires the automation. Changing it detaches the automation from its bound post or story (a post id and a story id are different objects), unless this same request sets a new binding. Every trigger but 'comment' is Instagram only; 'story_mention' also requires no keywords and no binding. (enum: comment, live_comment, story_reply, story_mention) | [optional]
**keywords** | Option<**Vec<String>**> |  | [optional]
**match_mode** | Option<**MatchMode**> | How a keyword is compared with the comment. 'contains' (default) matches anywhere, even inside another word (keyword 'app' fires on 'happy'). 'word' matches the keyword only as a standalone word. 'exact' requires the whole comment to be exactly the keyword. (enum: exact, contains, word) | [optional]
**exclude_keywords** | Option<**Vec<String>**> | Comments containing one of these never trigger the automation, even when a trigger keyword also matches. Compared using the same matchMode. | [optional]
**typo_tolerance** | Option<**bool**> | Only with matchMode=word: also fire on close misspellings of a keyword (one edit for 4-7 character keywords, two from 8 up). Keywords shorter than 4 characters are never fuzzy-matched. | [optional]
**platform_post_id** | Option<**String**> | Re-binds the automation to another post: the platform media/post ID (or story media id when trigger=story_reply). postId, platformPostId and postTitle move as a unit: sending any of them replaces all three, and an omitted one is cleared. Send all three as null (or empty) to make it account-wide (any post / any story). Omit all three to keep the current binding. 409 when another active automation already owns the new post. | [optional]
**post_id** | Option<**String**> | Zernio post ID (24 hexadecimal characters); platform IDs return 400. Use it INSTEAD of platformPostId to bind to a not-yet-published Zernio post: the automation stays pending and arms itself when that post publishes. Moves as a unit with platformPostId and postTitle (see platformPostId). | [optional]
**post_title** | Option<**String**> | Post content snippet for display. Moves as a unit with platformPostId and postId (see platformPostId). | [optional]
**dm_message** | Option<**String**> |  | [optional]
**buttons** | Option<[**Vec<models::DmButton>**](DmButton.md)> | Inline DM buttons (1-3). Pass [] to clear all buttons. | [optional]
**template** | Option<[**models::CommentAutomationTemplate**](CommentAutomationTemplate.md)> |  | [optional]
**comment_reply** | Option<**String**> |  | [optional]
**dm_message_variations** | Option<**Vec<String>**> | Alternate DM texts for random rotation (see create). Pass [] to clear. | [optional]
**comment_reply_variations** | Option<**Vec<String>**> | Alternate public replies for random rotation. Pass [] to clear. | [optional]
**link_tracking** | Option<**bool**> | Wrap link buttons in a tracked redirect to count clicks. Pass false to send links untouched. | [optional]
**click_tag** | Option<**String**> | Tag applied to a contact when they click a tracked link (requires linkTracking). Empty string clears it. | [optional]
**also_match_in_dms** | Option<**bool**> | Also fire these keywords on a plain inbound DM. Enabling it requires the automation to end up with at least one keyword (this request's keywords if you send them, otherwise the stored ones) and is rejected on story_reply automations. | [optional]
**dm_delay_seconds** | Option<**i32**> | Seconds to wait after the trigger before sending the DM. Send 0 to clear the delay and reply immediately. | [optional]
**comment_reply_delay_seconds** | Option<**i32**> | Seconds to wait before posting the public comment reply. Send 0 to clear it. The reply never goes out before the DM. | [optional]
**audience** | Option<[**models::CommentAutomationAudience**](CommentAutomationAudience.md)> |  | [optional]
**follow_gate** | Option<[**models::CommentAutomationFollowGate**](CommentAutomationFollowGate.md)> |  | [optional]
**is_active** | Option<**bool**> |  | [optional]
**repeat_policy** | Option<[**models::CommentAutomationRepeatPolicy**](CommentAutomationRepeatPolicy.md)> |  | [optional]
**dedupe_same_text_hours** | Option<**i32**> | Skip the DM when this recipient already received identical DM text (after personalisation) from this account, from any automation, within this many hours. The skip is logged with status skipped. Send null to clear. | [optional]
**public_reply_policy** | Option<**PublicReplyPolicy**> | 'after_dm' posts commentReply only after a successful DM. 'always' posts it whatever the audience rule, dedupe or DM outcome: the moment a comment matches, or after commentReplyDelaySeconds when set (raised to dmDelaySeconds, so it never precedes the DM attempt). (enum: after_dm, always) | [optional]
**actions** | Option<[**models::CommentAutomationActions**](CommentAutomationActions.md)> |  | [optional]
**quick_replies** | Option<[**Vec<models::CommentAutomationQuickReply>**](CommentAutomationQuickReply.md)> | Opt-in quick-reply chips on the DM (up to 13). Chips do not render in Message Requests, where a first DM to a cold commenter lands, so prefer buttons for first contact. Mutually exclusive with buttons and template (400). Send null to clear. | [optional]
**dm_media** | Option<[**models::CommentAutomationDmMedia**](CommentAutomationDmMedia.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


