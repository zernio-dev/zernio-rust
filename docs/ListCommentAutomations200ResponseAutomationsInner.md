# ListCommentAutomations200ResponseAutomationsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**platform** | Option<**Platform**> |  (enum: instagram, facebook, tiktok, threads, linkedin, youtube) | [optional]
**trigger** | Option<**Trigger**> |  (enum: comment, live_comment, story_reply, story_mention) | [optional]
**account_id** | Option<**String**> |  | [optional]
**platform_post_id** | Option<**String**> |  | [optional]
**post_title** | Option<**String**> |  | [optional]
**post_id** | Option<**String**> |  | [optional]
**keywords** | Option<**Vec<String>**> |  | [optional]
**match_mode** | Option<**MatchMode**> | How a keyword is compared with the comment. 'contains' (default) matches anywhere, even inside another word (keyword 'app' fires on 'happy'). 'word' matches the keyword only as a standalone word. 'exact' requires the whole comment to be exactly the keyword. (enum: exact, contains, word) | [optional]
**exclude_keywords** | Option<**Vec<String>**> | Comments containing one of these never trigger the automation, even when a trigger keyword also matches. Compared using the same matchMode. | [optional]
**typo_tolerance** | Option<**bool**> | Only with matchMode=word: also fire on close misspellings of a keyword (one edit for 4-7 character keywords, two from 8 up). Keywords shorter than 4 characters are never fuzzy-matched. | [optional]
**dm_message** | Option<**String**> | Instagram and Facebook only. On reply-only platforms (tiktok, threads, linkedin, youtube) every DM-leg field is omitted: dmMessage, dmMessageVariations, buttons, template, quickReplies, dmMedia, publicReplyPolicy, dedupeSameTextHours, actions, audience, followGate, dmDelaySeconds and alsoMatchInDms. | [optional]
**buttons** | Option<[**Vec<models::DmButton>**](DmButton.md)> | Inline DM buttons (up to 3). Omitted when none are set. | [optional]
**template** | Option<[**models::CommentAutomationTemplate**](CommentAutomationTemplate.md)> |  | [optional]
**comment_reply** | Option<**String**> |  | [optional]
**dm_message_variations** | Option<**Vec<String>**> | Alternate DM texts rotated at random with dmMessage. Omitted when none. | [optional]
**comment_reply_variations** | Option<**Vec<String>**> | Alternate public replies rotated at random with commentReply. Omitted when none. | [optional]
**link_tracking** | Option<**bool**> | Whether link buttons in the DM are wrapped in a tracked redirect to count clicks. | [optional]
**click_tag** | Option<**String**> | Tag applied to a contact when they click a tracked link. | [optional]
**dm_delay_seconds** | Option<**i32**> | Seconds waited after the trigger before the DM is sent. Absent when the DM goes out immediately. | [optional]
**comment_reply_delay_seconds** | Option<**i32**> | Seconds waited before the public reply is posted. Absent when it follows the DM immediately. | [optional]
**also_match_in_dms** | Option<**bool**> | Whether these keywords also fire on a plain inbound DM. | [optional]
**repeat_policy** | Option<[**models::CommentAutomationRepeatPolicy**](CommentAutomationRepeatPolicy.md)> |  | [optional]
**dedupe_same_text_hours** | Option<**i32**> | Same-text dedupe window in hours. Omitted when off. | [optional]
**public_reply_policy** | Option<**PublicReplyPolicy**> |  (enum: after_dm, always) | [optional]
**actions** | Option<[**models::CommentAutomationActions**](CommentAutomationActions.md)> |  | [optional]
**quick_replies** | Option<[**Vec<models::CommentAutomationQuickReply>**](CommentAutomationQuickReply.md)> |  | [optional]
**dm_media** | Option<[**models::CommentAutomationDmMedia**](CommentAutomationDmMedia.md)> |  | [optional]
**audience** | Option<[**models::CommentAutomationAudience**](CommentAutomationAudience.md)> |  | [optional]
**follow_gate** | Option<[**models::CommentAutomationFollowGate**](CommentAutomationFollowGate.md)> |  | [optional]
**is_active** | Option<**bool**> |  | [optional]
**stats** | Option<[**models::CommentAutomationStats**](CommentAutomationStats.md)> |  | [optional]
**created_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


