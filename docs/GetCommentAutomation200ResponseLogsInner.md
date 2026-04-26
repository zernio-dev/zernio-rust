# GetCommentAutomation200ResponseLogsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**comment_id** | Option<**String**> |  | [optional]
**commenter_id** | Option<**String**> |  | [optional]
**commenter_name** | Option<**String**> |  | [optional]
**comment_text** | Option<**String**> |  | [optional]
**status** | Option<**Status**> | DM outcome (enum: sent, failed, skipped) | [optional]
**error** | Option<**String**> | DM error message if status is failed | [optional]
**comment_reply_status** | Option<**CommentReplyStatus**> | Outcome of the optional public reply on the triggering comment. 'skipped' if no commentReply was configured or if the DM failed (the public reply is not attempted in that case). (enum: sent, failed, skipped) | [optional]
**comment_reply_error** | Option<**String**> | Public-reply error message if commentReplyStatus is failed | [optional]
**created_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


