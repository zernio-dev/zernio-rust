# RedditPost

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Reddit post ID (without type prefix) | [optional]
**fullname** | Option<**String**> | Reddit fullname (e.g. t3_abc123) | [optional]
**title** | Option<**String**> |  | [optional]
**author** | Option<**String**> |  | [optional]
**subreddit** | Option<**String**> |  | [optional]
**url** | Option<**String**> | Post URL (may be a gallery URL | [optional]
**permalink** | Option<**String**> | Full permalink to the Reddit post | [optional]
**selftext** | Option<**String**> | Self-post body text (empty string for link posts) | [optional]
**created_utc** | Option<**f64**> | Unix timestamp of post creation | [optional]
**score** | Option<**i32**> |  | [optional]
**num_comments** | Option<**i32**> |  | [optional]
**over18** | Option<**bool**> | Whether the post is marked NSFW | [optional]
**stickied** | Option<**bool**> |  | [optional]
**flair_text** | Option<**String**> | Link flair text if set | [optional]
**is_gallery** | Option<**bool**> | Whether the post is a gallery with multiple images | [optional]
**gallery_images** | Option<**Vec<String>**> | Individual image URLs for gallery posts (only present when isGallery is true) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


