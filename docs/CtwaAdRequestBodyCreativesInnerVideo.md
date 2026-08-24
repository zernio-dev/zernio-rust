# CtwaAdRequestBodyCreativesInnerVideo

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | Option<**String**> | Public URL of the video to upload. Provide either `url` or `id`. | [optional]
**id** | Option<**String**> | Reuse a video already uploaded to this ad account (list them with GET /v1/ads/videos) instead of re-uploading. Wins over `url`. Provide either `url` or `id`. | [optional]
**thumbnail_url** | Option<**String**> | OPTIONAL: when omitted, the poster is auto-generated from Meta's own preferred video thumbnail. When Meta produces no candidate the request fails with a 502 platform_error (reason: video_thumbnail_unavailable).  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


