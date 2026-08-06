# CommentAutomationAudience

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**follower_status** | Option<**FollowerStatus**> |  (enum: any, follower, non_follower) | [optional][default to Any]
**min_follower_count** | Option<**i32**> | Skip commenters with fewer followers than this. Omit for no size rule. | [optional]
**when_unknown** | Option<**WhenUnknown**> | What to do when Instagram will not reveal the follow relationship.   * `send` (default) - deliver the DM anyway (fails open).   * `skip` - stay silent.   * `verify` - send `followGate.message` with a confirm button. Tapping it is a     message, which grants consent, so the re-check on the tap resolves and the     real DM (or `followGate.notFollowingMessage`) follows automatically.  (enum: send, skip, verify) | [optional][default to Send]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


