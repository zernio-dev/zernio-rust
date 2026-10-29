# InstagramVideoFallback

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**kind** | **Kind** |  (enum: instagram_video_reuploaded, instagram_video_rehosted_copy) | 
**linked_to_original_post** | **bool** | True when the ad still references the original Instagram post and keeps its engagement. | 
**video_id** | **String** | The Facebook-side ad video Zernio made.  - instagram_video_reuploaded: the copy in the ad account video library (possibly one made by an earlier boost of the same media, reused). The creative carries it as video_id, unless Meta accepted the plain post reference once the copy existed; then the copy is kept for that reference. - instagram_video_rehosted_copy: the new upload the creative uses (an unused copy made by this request is deleted). | 
**platform_error** | [**models::InstagramVideoFallbackPlatformError**](InstagramVideoFallbackPlatformError.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


