# CreateCommentAutomation200ResponseAutomation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**platform** | Option<**String**> |  | [optional]
**platform_post_id** | Option<**String**> |  | [optional]
**keywords** | Option<**Vec<String>**> |  | [optional]
**match_mode** | Option<**MatchMode**> |  (enum: exact, contains) | [optional]
**dm_message** | Option<**String**> |  | [optional]
**buttons** | Option<[**Vec<models::DmButton>**](DmButton.md)> | Inline DM buttons (up to 3). Omitted when none are set. | [optional]
**comment_reply** | Option<**String**> |  | [optional]
**is_active** | Option<**bool**> |  | [optional]
**stats** | Option<[**models::CreateCommentAutomation200ResponseAutomationStats**](CreateCommentAutomation200ResponseAutomationStats.md)> |  | [optional]
**created_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


