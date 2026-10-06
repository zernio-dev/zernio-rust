# CommentAutomationLog

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**comment_id** | Option<**String**> |  | [optional]
**commenter_id** | Option<**String**> |  | [optional]
**commenter_name** | Option<**String**> |  | [optional]
**commenter_username** | Option<**String**> |  | [optional]
**comment_text** | Option<**String**> |  | [optional]
**source** | Option<**Source**> | Which door triggered this send. Null on rows written before this field existed (all of those are comment-triggered). (enum: comment, live_comment, story_reply, story_mention, dm, ) | [optional]
**status** | Option<**Status**> | DM outcome. 'pending' = the automation has a dmDelaySeconds and the response is queued but not sent yet. 'gated' = the follow-gate confirmation DM went out and we are waiting for the tap; it flips to 'sent' or 'skipped' when they tap. 'skipped' also covers repeatPolicy, cooldown and dedupeSameTextHours suppressions, with the reason in error. (enum: pending, sent, failed, skipped, gated) | [optional]
**audience_outcome** | Option<**AudienceOutcome**> | How the audience rule resolved. Null on automations without one. (enum: passed, blocked, gate_sent, gate_passed, gate_failed, ) | [optional]
**gate_button_status** | Option<**GateButtonStatus**> | Whether the follow-gate button reached the commenter: 'rejected' = Meta refused the gate DM, 'omitted' = the prompt went out as plain text because it was over 640 characters. Null when no gate DM was sent. (enum: delivered, rejected, omitted, ) | [optional]
**commenter_is_follower** | Option<**bool**> | Follow relationship at decision time. Null when Instagram would not tell us (the commenter never messaged the account). | [optional]
**commenter_follower_count** | Option<**i32**> |  | [optional]
**gate_resolved_at** | Option<**String**> | When the follow-gate tap was claimed. | [optional]
**error** | Option<**String**> | DM error message when status is failed, or the reason when it is skipped. | [optional]
**platform_error** | Option<[**models::CommentAutomationLogPlatformError**](CommentAutomationLogPlatformError.md)> |  | [optional]
**private_reply_consumed** | Option<**bool**> | True when the failed send spent the comment's single private reply (Instagram subcode 1545133 or 2534023, or Meta code 10900 on Instagram and Facebook), the same rule as `details.privateReplyConsumed` on the private-reply endpoint. Null on direct DMs and on rows written before this field existed. | [optional]
**comment_reply_status** | Option<**CommentReplyStatus**> | Outcome of the optional public reply on the triggering comment. With publicReplyPolicy after_dm, 'skipped' if no commentReply was configured or if the DM failed (the public reply is not attempted in that case). (enum: pending, sent, failed, skipped, ) | [optional]
**comment_reply_error** | Option<**String**> | Public-reply error message if commentReplyStatus is failed | [optional]
**public_reply_posted_at** | Option<**String**> | When the public reply was posted. Null when it was not. | [optional]
**like_skipped** | Option<**String**> | Why actions.likeComment did not like the comment. Null when it did or was not configured. | [optional]
**hide_skipped** | Option<**String**> | Why actions.hideComment did not hide the comment. Null when it did or was not configured. | [optional]
**media_error** | Option<**String**> | Why the dmMedia follow-up was not delivered. The DM itself still counts as sent. | [optional]
**next_due_at** | Option<**String**> | When the next queued send fires. Present only while something is still pending. | [optional]
**clicked_at** | Option<**String**> | This recipient's first click on a tracked link (what uniqueClicks counts). | [optional]
**click_count** | Option<**i32**> | This recipient's total clicks on tracked links. | [optional]
**created_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


