# CreateCommentAutomation200ResponseAutomation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**platform** | Option<**String**> |  | [optional]
**trigger** | Option<**Trigger**> |  (enum: comment, story_reply) | [optional]
**platform_post_id** | Option<**String**> |  | [optional]
**keywords** | Option<**Vec<String>**> |  | [optional]
**match_mode** | Option<**MatchMode**> | How a keyword is compared with the comment. 'contains' (default) matches anywhere, even inside another word (keyword 'app' fires on 'happy'). 'word' matches the keyword only as a standalone word. 'exact' requires the whole comment to be exactly the keyword. (enum: exact, contains, word) | [optional]
**exclude_keywords** | Option<**Vec<String>**> | Comments containing one of these never trigger the automation, even when a trigger keyword also matches. Compared using the same matchMode. | [optional]
**typo_tolerance** | Option<**bool**> | Only with matchMode=word: also fire on close misspellings of a keyword (one edit for 4-7 character keywords, two from 8 up). Keywords shorter than 4 characters are never fuzzy-matched. | [optional]
**dm_message** | Option<**String**> |  | [optional]
**buttons** | Option<[**Vec<models::DmButton>**](DmButton.md)> | Inline DM buttons (up to 3). Omitted when none are set. | [optional]
**comment_reply** | Option<**String**> |  | [optional]
**dm_message_variations** | Option<**Vec<String>**> | Alternate DM texts rotated at random with dmMessage. Omitted when none. | [optional]
**comment_reply_variations** | Option<**Vec<String>**> | Alternate public replies rotated at random with commentReply. Omitted when none. | [optional]
**link_tracking** | Option<**bool**> |  | [optional]
**click_tag** | Option<**String**> |  | [optional]
**is_active** | Option<**bool**> |  | [optional]
**stats** | Option<[**models::CreateCommentAutomation200ResponseAutomationStats**](CreateCommentAutomation200ResponseAutomationStats.md)> |  | [optional]
**created_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


