# GetInboxPostComments200ResponsePost

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Facebook post id ({pageId}_{postId}) or Instagram media id | 
**fullname** | Option<**String**> | Fullname with type prefix (e.g. \"t3_1tjtj26\") | [optional]
**title** | Option<**String**> |  | [optional]
**selftext** | Option<**String**> | Body text for self-posts (empty for link posts) | [optional]
**author** | Option<**String**> | Reddit username, without the u/ prefix | [optional]
**subreddit** | Option<**String**> | Subreddit name, without the r/ prefix | [optional]
**permalink** | **String** |  | 
**url** | Option<**String**> | For link posts, the external URL; for self-posts, the Reddit permalink | [optional]
**score** | Option<**i32**> | Net upvotes (upvotes minus downvotes) | [optional]
**num_comments** | Option<**i32**> |  | [optional]
**created_utc** | Option<**i32**> | Unix timestamp in seconds | [optional]
**over18** | Option<**bool**> |  | [optional]
**stickied** | Option<**bool**> |  | [optional]
**flair_text** | Option<**String**> | Link flair text if any | [optional]
**is_gallery** | Option<**bool**> | True if the post is a Reddit gallery (multiple images) | [optional]
**text** | **String** | Facebook post message or Instagram caption | 
**thumbnail_url** | **String** | Facebook `full_picture` (or the first attachment image); Instagram `thumbnail_url` for videos, `media_url` for images. Expiring Meta CDN URL. | 
**media_url** | **String** | Instagram `media_url` (the video file for videos). Always null on Facebook. Expiring Meta CDN URL. | 
**media_type** | **String** | Instagram `media_type` (IMAGE, VIDEO, CAROUSEL_ALBUM) or the Facebook attachment type (photo, video_inline, link, ...) | 
**product_type** | **String** | Instagram `media_product_type`: AD, FEED, REELS or STORY. Always null on Facebook. | 
**created_at** | **String** | Creation time as Meta returns it (e.g. 2026-05-27T17:15:51+0000) | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


