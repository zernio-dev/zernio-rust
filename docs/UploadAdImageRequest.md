# UploadAdImageRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant); its platform decides where the campaign is created. | 
**ad_account_id** | **String** | Platform ad account id (Meta act_<n>, Google customer id, LinkedIn account id, ...). | 
**image_base64** | **String** | Raw base64 image bytes, or a full data URL (the data:image/...;base64, prefix is stripped). | 
**filename** | Option<**String**> | Optional filename shown in Meta's image library. Defaults to ad_image.jpg. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


