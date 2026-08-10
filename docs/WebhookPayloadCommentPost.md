# WebhookPayloadCommentPost

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Internal post ID (null for posts not published through Zernio) | 
**platform_post_id** | **String** | Platform's post ID | 
**content** | Option<**String**> | Post text, from our synced copy — no platform call is made on the comment path, so null when the post was never synced. | 
**image_url** | Option<**String**> | Post thumbnail or first media item URL. Platform CDN URLs expire, fetch promptly. | 
**permalink** | Option<**String**> | Public URL of the post. Null for posts published through Zernio that were never re-synced. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


