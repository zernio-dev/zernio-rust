# UploadFileRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** |  | 
**name** | **String** |  | 
**content_type** | **String** |  | 
**parent_id** | Option<**String**> | Target folder; the root when omitted. | [optional]
**url** | **String** |  | 
**convert_to** | Option<**ConvertTo**> | Google Drive only: import the bytes as a Docs, Sheets or Slides file (a text or Office file becomes an editable document). OneDrive answers 400. (enum: application/vnd.google-apps.document, application/vnd.google-apps.spreadsheet, application/vnd.google-apps.presentation) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


