# InstagramBusinessDiscoveryMediaInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**caption** | Option<**String**> |  | 
**media_type** | Option<**String**> | IMAGE, VIDEO or CAROUSEL_ALBUM | 
**media_product_type** | Option<**String**> | FEED or REELS | 
**timestamp** | Option<**String**> |  | 
**permalink** | Option<**String**> |  | 
**like_count** | Option<**i32**> | Null when the owner hides like counts | 
**comments_count** | Option<**i32**> |  | 
**media_url** | Option<**String**> | Temporary CDN URL that expires; download the file rather than storing the link. Null on videos whose audio is licensed music, use thumbnailUrl for the cover. | 
**thumbnail_url** | Option<**String**> | Video cover frame, VIDEO only. Temporary CDN URL. | 
**view_count** | Option<**i32**> | Reels only. Null on images and carousels. | 
**children** | Option<[**Vec<models::InstagramBusinessDiscoveryMediaInnerChildrenInner>**](InstagramBusinessDiscoveryMediaInnerChildrenInner.md)> | Carousel slides in order. Null unless mediaType is CAROUSEL_ALBUM. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


