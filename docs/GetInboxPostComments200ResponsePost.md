# GetInboxPostComments200ResponsePost

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Reddit post base36 id (e.g. \"1tjtj26\") | [optional]
**fullname** | Option<**String**> | Fullname with type prefix (e.g. \"t3_1tjtj26\") | [optional]
**title** | Option<**String**> |  | [optional]
**selftext** | Option<**String**> | Body text for self-posts (empty for link posts) | [optional]
**author** | Option<**String**> | Reddit username | [optional]
**subreddit** | Option<**String**> | Subreddit name | [optional]
**permalink** | Option<**String**> | Absolute URL to the post on reddit.com | [optional]
**url** | Option<**String**> | For link posts | [optional]
**score** | Option<**i32**> | Net upvotes (upvotes minus downvotes) | [optional]
**num_comments** | Option<**i32**> |  | [optional]
**created_utc** | Option<**i32**> | Unix timestamp in seconds | [optional]
**over18** | Option<**bool**> |  | [optional]
**stickied** | Option<**bool**> |  | [optional]
**flair_text** | Option<**String**> | Link flair text if any | [optional]
**is_gallery** | Option<**bool**> | True if the post is a Reddit gallery (multiple images) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


