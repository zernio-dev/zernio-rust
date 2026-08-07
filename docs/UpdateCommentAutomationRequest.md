# UpdateCommentAutomationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | Option<**String**> |  | [optional]
**trigger** | Option<**Trigger**> | What fires the automation. Changing it detaches the automation from its bound post or story (a post id and a story id are different objects), unless this same request sets a new binding. 'story_reply' is Instagram only. (enum: comment, story_reply) | [optional]
**keywords** | Option<**Vec<String>**> |  | [optional]
**match_mode** | Option<**MatchMode**> | How a keyword is compared with the comment. 'contains' (default) matches anywhere, even inside another word (keyword 'app' fires on 'happy'). 'word' matches the keyword only as a standalone word. 'exact' requires the whole comment to be exactly the keyword. (enum: exact, contains, word) | [optional]
**exclude_keywords** | Option<**Vec<String>**> | Comments containing one of these never trigger the automation, even when a trigger keyword also matches. Compared using the same matchMode. | [optional]
**typo_tolerance** | Option<**bool**> | Only with matchMode=word: also fire on close misspellings of a keyword (one edit for 4-7 character keywords, two from 8 up). Keywords shorter than 4 characters are never fuzzy-matched. | [optional]
**dm_message** | Option<**String**> |  | [optional]
**buttons** | Option<[**Vec<models::DmButton>**](DmButton.md)> | Inline DM buttons (1-3). Pass [] to clear all buttons. | [optional]
**template** | Option<[**models::CommentAutomationTemplate**](CommentAutomationTemplate.md)> |  | [optional]
**comment_reply** | Option<**String**> |  | [optional]
**dm_message_variations** | Option<**Vec<String>**> | Alternate DM texts for random rotation (see create). Pass [] to clear. | [optional]
**comment_reply_variations** | Option<**Vec<String>**> | Alternate public replies for random rotation. Pass [] to clear. | [optional]
**link_tracking** | Option<**bool**> | Wrap link buttons in a tracked redirect to count clicks. Pass false to send links untouched. | [optional]
**click_tag** | Option<**String**> | Tag applied to a contact when they click a tracked link (requires linkTracking). Empty string clears it. | [optional]
**dm_delay_seconds** | Option<**i32**> | Seconds to wait after the trigger before sending the DM. Send 0 to clear the delay and reply immediately. | [optional]
**comment_reply_delay_seconds** | Option<**i32**> | Seconds to wait before posting the public comment reply. Send 0 to clear it. The reply never goes out before the DM. | [optional]
**audience** | Option<[**models::CommentAutomationAudience**](CommentAutomationAudience.md)> |  | [optional]
**follow_gate** | Option<[**models::CommentAutomationFollowGate**](CommentAutomationFollowGate.md)> |  | [optional]
**is_active** | Option<**bool**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


