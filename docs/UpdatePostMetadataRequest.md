# UpdatePostMetadataRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **Platform** | The platform to update metadata on (enum: youtube) | 
**title** | Option<**String**> | New video title (max 100 characters for YouTube) | [optional]
**description** | Option<**String**> | New video description | [optional]
**tags** | Option<**Vec<String>**> | Array of keyword tags (max 500 characters combined for YouTube) | [optional]
**category_id** | Option<**String**> | YouTube video category ID | [optional]
**privacy_status** | Option<**PrivacyStatus**> | Video privacy setting (enum: public, private, unlisted) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


