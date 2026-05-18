# ListInstagramStories200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Instagram media ID of the story. | 
**media_type** | Option<**String**> | IMAGE / VIDEO / CAROUSEL_ALBUM | [optional]
**media_product_type** | Option<**String**> | Always 'STORY' for this endpoint. | [optional]
**media_url** | Option<**String**> | Direct media URL. Null if Meta flagged the story for copyright. URL expires when the story expires. | [optional]
**permalink** | Option<**String**> | Public Instagram permalink to the story (only viewable while live). | [optional]
**thumbnail_url** | Option<**String**> | Thumbnail URL for video stories. | [optional]
**timestamp** | Option<**String**> | When the story was posted. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


