# GetTikTokSmartPlusAdReview200ResponseMaterialsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ad_material_id** | Option<**String**> | TikTok `ad_material_id` of the creative inside this ad. | [optional]
**material_type** | Option<**MaterialType**> | Null for a creative TikTok added on its own or a carousel image. (enum: spark_post, video, carousel, catalog_carousel, ) | [optional]
**tiktok_item_id** | Option<**String**> | The TikTok post id when the creative is a Spark post. | [optional]
**video_id** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**operation_status** | Option<**String**> | TikTok `material_operation_status`: ENABLE or DISABLE. | [optional]
**review_status** | Option<[**models::TikTokSmartPlusReviewStatus**](TikTokSmartPlusReviewStatus.md)> |  | [optional]
**raw_review_status** | Option<**String**> | TikTok `review_status`, verbatim. | [optional]
**reject_reasons** | Option<**Vec<String>**> | Every distinct reason across `rejections`. Empty when approved. | [optional]
**passed_locations** | Option<**Vec<String>**> |  | [optional]
**rejections** | Option<[**Vec<models::TikTokReviewRejection>**](TikTokReviewRejection.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


