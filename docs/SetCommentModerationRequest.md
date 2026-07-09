# SetCommentModerationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | The social account ID | 
**platform** | **Platform** | Only YouTube supports comment moderation (enum: youtube) | 
**moderation_status** | **ModerationStatus** | published approves the comment, rejected removes it, heldForReview returns it to the queue. (enum: published, rejected, heldForReview) | 
**ban_author** | Option<**bool**> | Also ban the comment's author, auto-rejecting their future comments. Only valid when moderationStatus is \"rejected\"; any other pairing is a 400.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


