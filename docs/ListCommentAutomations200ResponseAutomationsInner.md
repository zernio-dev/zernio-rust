# ListCommentAutomations200ResponseAutomationsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**platform** | Option<**Platform**> |  (enum: instagram, facebook) | [optional]
**trigger** | Option<**Trigger**> |  (enum: comment, story_reply) | [optional]
**account_id** | Option<**String**> |  | [optional]
**platform_post_id** | Option<**String**> |  | [optional]
**post_title** | Option<**String**> |  | [optional]
**keywords** | Option<**Vec<String>**> |  | [optional]
**match_mode** | Option<**MatchMode**> |  (enum: exact, contains) | [optional]
**dm_message** | Option<**String**> |  | [optional]
**buttons** | Option<[**Vec<models::DmButton>**](DmButton.md)> | Inline DM buttons (up to 3). Omitted when none are set. | [optional]
**comment_reply** | Option<**String**> |  | [optional]
**dm_message_variations** | Option<**Vec<String>**> | Alternate DM texts rotated at random with dmMessage. Omitted when none. | [optional]
**comment_reply_variations** | Option<**Vec<String>**> | Alternate public replies rotated at random with commentReply. Omitted when none. | [optional]
**link_tracking** | Option<**bool**> | Whether link buttons in the DM are wrapped in a tracked redirect to count clicks. | [optional]
**click_tag** | Option<**String**> | Tag applied to a contact when they click a tracked link. | [optional]
**is_active** | Option<**bool**> |  | [optional]
**stats** | Option<[**models::ListCommentAutomations200ResponseAutomationsInnerStats**](ListCommentAutomations200ResponseAutomationsInnerStats.md)> |  | [optional]
**created_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


