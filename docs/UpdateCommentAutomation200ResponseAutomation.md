# UpdateCommentAutomation200ResponseAutomation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**keywords** | Option<**Vec<String>**> |  | [optional]
**match_mode** | Option<**MatchMode**> |  (enum: exact, contains) | [optional]
**dm_message** | Option<**String**> |  | [optional]
**buttons** | Option<[**Vec<models::DmButton>**](DmButton.md)> | Inline DM buttons (up to 3). Omitted when none are set. | [optional]
**comment_reply** | Option<**String**> |  | [optional]
**dm_message_variations** | Option<**Vec<String>**> | Alternate DM texts rotated at random with dmMessage. Omitted when none. | [optional]
**comment_reply_variations** | Option<**Vec<String>**> | Alternate public replies rotated at random with commentReply. Omitted when none. | [optional]
**is_active** | Option<**bool**> |  | [optional]
**updated_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


