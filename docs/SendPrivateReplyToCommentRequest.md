# SendPrivateReplyToCommentRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | The social account ID (Instagram or Facebook) | 
**message** | **String** | The message text to send as a private DM | 
**quick_replies** | Option<[**Vec<models::SendPrivateReplyToCommentRequestQuickRepliesInner>**](SendPrivateReplyToCommentRequestQuickRepliesInner.md)> | Optional quick-reply chips appended to the message. Visible only in the Instagram and Messenger apps (not on web). Maximum 13 entries. Mutually exclusive with `buttons`. Note: chips do NOT render in the Instagram Message Requests folder where DMs from non-followers land — use `buttons` instead for cold reach.  | [optional]
**buttons** | Option<[**Vec<models::SendPrivateReplyToCommentRequestButtonsInner>**](SendPrivateReplyToCommentRequestButtonsInner.md)> | Optional 1-3 inline buttons rendered as part of the same message bubble via Meta's button_template. Visible in the Instagram Message Requests folder (unlike quick replies). Mutually exclusive with `quickReplies`.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


