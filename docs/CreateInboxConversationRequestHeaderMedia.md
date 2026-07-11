# CreateInboxConversationRequestHeaderMedia

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **Type** | Must match the template header's media type. (enum: image, video, document) | 
**link** | Option<**String**> | Public URL of the asset to send. Must be reachable without auth. | [optional]
**id** | Option<**String**> | A Meta media id (from the media upload endpoint), as an alternative to link. | [optional]
**filename** | Option<**String**> | Document display name shown to the recipient (e.g. \"Factura 0001-123.pdf\"). document type only; ignored for image/video. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


