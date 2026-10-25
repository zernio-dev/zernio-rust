# GetAccountPosts200ResponsePostsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | The platform's own post id (the video ID on YouTube) | [optional]
**platform** | Option<**String**> |  | [optional]
**message** | Option<**String**> | Caption or title, empty string when the post has no text | [optional]
**created_time** | Option<**String**> |  | [optional]
**permalink** | Option<**String**> | Public URL of the post on the platform | [optional]
**picture** | Option<**String**> | Thumbnail or media URL | [optional]
**media_type** | Option<**String**> |  | [optional]
**comment_count** | Option<**i32**> |  | [optional]
**like_count** | Option<**i32**> |  | [optional]
**reaction_count** | Option<**i32**> | Facebook and LinkedIn only | [optional]
**share_count** | Option<**i32**> |  | [optional]
**cid** | Option<**String**> | Bluesky content id, required to reply to the post | [optional]
**subreddit** | Option<**String**> | Reddit only | [optional]
**title** | Option<**String**> | Pinterest only: native Pin title | [optional]
**description** | Option<**String**> | Pinterest only: full native Pin description (Pinterest caps it at 800 characters) | [optional]
**link** | Option<**String**> | Pinterest only: destination URL of the Pin, not the Pin page (see permalink) | [optional]
**board_id** | Option<**String**> | Pinterest only: id of the board holding the Pin | [optional]
**board_owner_username** | Option<**String**> | Pinterest only: username of the board owner | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


