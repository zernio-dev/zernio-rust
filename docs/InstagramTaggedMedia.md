# InstagramTaggedMedia

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Instagram media ID of the post the account is tagged in. | 
**caption** | Option<**String**> |  | 
**media_type** | Option<**String**> | IMAGE, VIDEO or CAROUSEL_ALBUM. | 
**media_product_type** | Option<**String**> | FEED or REELS. | 
**media_url** | Option<**String**> | Temporary CDN URL. Meta omits it for videos with copyrighted audio, flagged videos and reels whose owner disabled downloads. | 
**thumbnail_url** | Option<**String**> | Cover image of a video or reel. | 
**permalink** | Option<**String**> | Public Instagram URL of the post. | 
**timestamp** | Option<**String**> | Publication time as Meta returns it (ISO 8601). | 
**username** | Option<**String**> | Instagram handle of the account that posted the media and tagged yours. | 
**like_count** | Option<**i32**> | Null when the owner hides like counts. | 
**comments_count** | Option<**i32**> |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


