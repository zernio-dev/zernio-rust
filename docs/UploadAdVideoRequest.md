# UploadAdVideoRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. | 
**ad_account_id** | **String** | Meta ad account id (act_<n>). | 
**video_url** | Option<**String**> | Public https URL of the video; downloaded server-side (SSRF-guarded) before chunked upload. Provide exactly one of videoUrl or videoBase64. | [optional]
**video_base64** | Option<**String**> | Raw base64 video bytes, or a full data URL (the data:video/...;base64, prefix is stripped). Capped by Vercel's body limit (~4.5 MB payload). Provide exactly one of videoUrl or videoBase64. | [optional]
**filename** | Option<**String**> | Optional filename shown alongside the upload session. Applied only when uploading via videoBase64. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


