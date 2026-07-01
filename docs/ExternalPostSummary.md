# ExternalPostSummary

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | Option<**String**> | Platform the post belongs to (e.g. instagram, youtube, tiktok) | [optional]
**platform_post_id** | Option<**String**> | The platform's own post/media/video id | [optional]
**platform_post_url** | Option<**String**> | Canonical URL (permalink) of the post on the platform | [optional]
**content** | Option<**String**> | Post caption / text | [optional]
**published_at** | Option<**String**> | When the post was published on the platform | [optional]
**media_type** | Option<**String**> | Media type (e.g. image, video, carousel) | [optional]
**media_url** | Option<**String**> | Primary media URL | [optional]
**thumbnail_url** | Option<**String**> | Thumbnail URL | [optional]
**media_items** | Option<**Vec<serde_json::Value>**> | Per-item media (for carousels / multi-media posts) | [optional]
**analytics** | Option<[**models::ExternalPostSummaryAnalytics**](ExternalPostSummaryAnalytics.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


