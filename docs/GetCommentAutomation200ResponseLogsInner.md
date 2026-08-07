# GetCommentAutomation200ResponseLogsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**comment_id** | Option<**String**> |  | [optional]
**commenter_id** | Option<**String**> |  | [optional]
**commenter_name** | Option<**String**> |  | [optional]
**comment_text** | Option<**String**> |  | [optional]
**status** | Option<**Status**> | DM outcome. 'pending' = the automation has a dmDelaySeconds and the response is queued but not sent yet. 'gated' = the follow-gate confirmation DM went out and we are waiting for the tap; it flips to 'sent' or 'skipped' when they tap. (enum: pending, sent, failed, skipped, gated) | [optional]
**audience_outcome** | Option<**AudienceOutcome**> | How the audience rule resolved. Absent on automations without one. (enum: passed, blocked, gate_sent, gate_passed, gate_failed) | [optional]
**commenter_is_follower** | Option<**bool**> | Follow relationship at decision time. Absent when Instagram would not tell us (the commenter never messaged the account). | [optional]
**commenter_follower_count** | Option<**i32**> |  | [optional]
**error** | Option<**String**> | DM error message if status is failed | [optional]
**comment_reply_status** | Option<**CommentReplyStatus**> | Outcome of the optional public reply on the triggering comment. 'skipped' if no commentReply was configured or if the DM failed (the public reply is not attempted in that case). (enum: sent, failed, skipped) | [optional]
**comment_reply_error** | Option<**String**> | Public-reply error message if commentReplyStatus is failed | [optional]
**next_due_at** | Option<**String**> | When the next queued send fires. Present only while something is still pending. | [optional]
**created_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


