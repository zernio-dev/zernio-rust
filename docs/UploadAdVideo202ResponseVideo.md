# UploadAdVideo202ResponseVideo

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Meta video id. Usable as video.id once GET /v1/ads/videos/{videoId} reports ready. | [optional]
**status** | Option<**Status**> |  (enum: processing) | [optional]
**thumbnail_url** | Option<**String**> | Always null on 202; read it from GET /v1/ads/videos/{videoId} once ready. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


