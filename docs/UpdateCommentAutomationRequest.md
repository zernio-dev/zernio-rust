# UpdateCommentAutomationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | Option<**String**> |  | [optional]
**keywords** | Option<**Vec<String>**> |  | [optional]
**match_mode** | Option<**MatchMode**> |  (enum: exact, contains) | [optional]
**dm_message** | Option<**String**> |  | [optional]
**buttons** | Option<[**Vec<models::DmButton>**](DmButton.md)> | Inline DM buttons (1-3). Pass [] to clear all buttons. | [optional]
**comment_reply** | Option<**String**> |  | [optional]
**is_active** | Option<**bool**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


