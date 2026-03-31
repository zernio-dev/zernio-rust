# UpdatePostMetadataRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **Platform** | The platform to update metadata on (enum: youtube) | 
**video_id** | Option<**String**> | YouTube video ID (required for direct mode, ignored for post-based mode) | [optional]
**account_id** | Option<**String**> | Zernio social account ID (required for direct mode, ignored for post-based mode) | [optional]
**title** | Option<**String**> | New video title (max 100 characters for YouTube) | [optional]
**description** | Option<**String**> | New video description | [optional]
**tags** | Option<**Vec<String>**> | Array of keyword tags (max 500 characters combined for YouTube) | [optional]
**category_id** | Option<**String**> | YouTube video category ID | [optional]
**privacy_status** | Option<**PrivacyStatus**> | Video privacy setting (enum: public, private, unlisted) | [optional]
**thumbnail_url** | Option<**String**> | Public URL of a custom thumbnail image (JPEG, PNG, or GIF, max 2 MB, recommended 1280x720). Works on any video you own, including existing videos not published through Zernio. The channel must be verified (phone verification) to set custom thumbnails. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


