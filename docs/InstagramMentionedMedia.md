# InstagramMentionedMedia

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Instagram media ID of the post whose caption mentions the account. | 
**caption** | Option<**String**> |  | 
**media_type** | Option<**String**> | IMAGE, VIDEO or CAROUSEL_ALBUM. | 
**media_url** | Option<**String**> | Temporary CDN URL. Meta omits it for videos with copyrighted or licensed audio and reels whose owner disabled downloads. | 
**timestamp** | Option<**String**> | Publication time as Meta returns it (ISO 8601). | 
**username** | Option<**String**> | Instagram handle of the account that posted the media and mentioned yours. | 
**like_count** | Option<**i32**> | Null when the owner hides like counts. | 
**comments_count** | Option<**i32**> |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


