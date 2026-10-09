# FacebookOrInstagramPost

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Facebook post id ({pageId}_{postId}) or Instagram media id | 
**permalink** | Option<**String**> |  | 
**text** | Option<**String**> | Facebook post message or Instagram caption | 
**thumbnail_url** | Option<**String**> | Facebook `full_picture` (or the first attachment image); Instagram `thumbnail_url` for videos, `media_url` for images. Expiring Meta CDN URL. | 
**media_url** | Option<**String**> | Instagram `media_url` (the video file for videos). Always null on Facebook. Expiring Meta CDN URL. | 
**media_type** | Option<**String**> | Instagram `media_type` (IMAGE, VIDEO, CAROUSEL_ALBUM) or the Facebook attachment type (photo, video_inline, link, ...) | 
**product_type** | Option<**String**> | Instagram `media_product_type`: AD, FEED, REELS or STORY. Always null on Facebook. | 
**created_at** | Option<**String**> | Creation time as Meta returns it (e.g. 2026-05-27T17:15:51+0000) | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


