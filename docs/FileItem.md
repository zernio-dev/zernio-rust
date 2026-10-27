# FileItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**account_id** | **String** |  | 
**provider** | **Provider** |  (enum: google, microsoft) | 
**name** | **String** |  | 
**kind** | **Kind** |  (enum: file, folder) | 
**mime_type** | Option<**String**> |  | 
**size** | Option<**i32**> | Bytes; null for folders and Google editors files. | 
**parent_id** | Option<**String**> |  | 
**web_url** | Option<**String**> | The provider's own link to open the item. | 
**downloadable** | **bool** | False for folders and for Drive files whose owner disabled downloading. | 
**export_mime_type** | Option<**String**> | Google Docs, Slides and Drawings download as PDF/PNG and Sheets as XLSX; this is the type the download carries. | [optional]
**created_at** | Option<**String**> |  | 
**modified_at** | Option<**String**> |  | 
**trashed** | **bool** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


