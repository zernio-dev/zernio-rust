# ListAdsInstagramPosts200ResponsePostsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Instagram media ID. Pass this as the existing-post id when creating an ad. | 
**caption** | Option<**String**> | Caption, when the media has one. | [optional]
**media_type** | **String** | Meta media_type, e.g. IMAGE, VIDEO or CAROUSEL_ALBUM. | 
**media_url** | Option<**String**> | Media URL. Meta omits it for some media types. | [optional]
**thumbnail_url** | Option<**String**> | Thumbnail URL. Present for VIDEO, where mediaUrl may be absent. | [optional]
**permalink** | Option<**String**> | Public Instagram permalink. | [optional]
**timestamp** | **String** | Publish time as Meta reports it. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


