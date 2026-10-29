# \FilesApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_file_picker_session**](FilesApi.md#create_file_picker_session) | **POST** /v1/files/picker-sessions | Create a hosted Google Picker session
[**create_folder**](FilesApi.md#create_folder) | **POST** /v1/files/folders | Create a folder
[**download_file**](FilesApi.md#download_file) | **GET** /v1/files/{fileId}/download | Download a file
[**get_file**](FilesApi.md#get_file) | **GET** /v1/files/{fileId} | Get a file or folder
[**get_file_share_link**](FilesApi.md#get_file_share_link) | **GET** /v1/files/{fileId}/share-link | Get an anyone-with-the-link share link
[**list_files**](FilesApi.md#list_files) | **GET** /v1/files | List files in a folder or search the drive
[**trash_file**](FilesApi.md#trash_file) | **DELETE** /v1/files/{fileId} | Move a file to the trash
[**update_file**](FilesApi.md#update_file) | **PATCH** /v1/files/{fileId} | Rename or move a file
[**upload_file**](FilesApi.md#upload_file) | **POST** /v1/files | Upload a file



## create_file_picker_session

> models::CreateFilePickerSession201Response create_file_picker_session(create_file_picker_session_request)
Create a hosted Google Picker session

Creates a hosted Google Picker session so your end user can grant Zernio access to Drive files.  Google accounts are connected with `drive.file`, so Zernio opens only files it created or the user picked (see the Files tag).  1. Create a session. 2. Send the user to `url`. 3. They pick files in Google Picker on a Zernio-hosted page.  ### Redirect  When they finish, the browser is sent to `redirectUrl` with these query params added (existing params are kept):  - `status=picked`, `pickerSessionId`, `fileIds` (comma-separated Drive file ids, already checked against Drive), or - `status=cancelled`, `pickerSessionId` when the user pressed Cancel.  A `file.picked` webhook fires on every successful pick, so `redirectUrl` is optional for server-side integrations. Closing the picker without picking keeps the session open; the user can try again until it expires.  ### Limits  - The URL is single-use and expires after 30 minutes; create a new session for every pick. - Google accounts only: Microsoft accounts answer 400 `platform_not_supported` because OneDrive needs no picker. - Picks are permanent grants: once picked, a file stays readable through the Files endpoints until the user removes Zernio from their Google account. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_file_picker_session_request** | [**CreateFilePickerSessionRequest**](CreateFilePickerSessionRequest.md) |  | [required] |

### Return type

[**models::CreateFilePickerSession201Response**](createFilePickerSession_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_folder

> models::UploadFile201Response create_folder(create_folder_request)
Create a folder

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_folder_request** | [**CreateFolderRequest**](CreateFolderRequest.md) |  | [required] |

### Return type

[**models::UploadFile201Response**](uploadFile_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## download_file

> std::path::PathBuf download_file(file_id, account_id)
Download a file

Streams the bytes with `Content-Disposition: attachment`. Google Docs, Slides and Drawings arrive as PDF/PNG and Sheets as XLSX, named with the export extension. Folders answer 400.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**file_id** | **String** |  | [required] |
**account_id** | **String** | The connected Google or Microsoft account. | [required] |

### Return type

[**std::path::PathBuf**](std::path::PathBuf.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/octet-stream, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_file

> models::UploadFile201Response get_file(file_id, account_id)
Get a file or folder

On Google Drive, a file Zernio neither created nor was given through Google Picker answers 404 `resource_not_found` with `details: { fileId, reason: file_not_granted }`; send the user through `POST /v1/files/picker-sessions` (pass the id in `fileIds` to show it first). The same 404 applies to download, update, trash and share-link.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**file_id** | **String** |  | [required] |
**account_id** | **String** | The connected Google or Microsoft account. | [required] |

### Return type

[**models::UploadFile201Response**](uploadFile_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_file_share_link

> models::GetFileShareLink200Response get_file_share_link(file_id, account_id)
Get an anyone-with-the-link share link

Grants read access to anyone holding the link (Drive `anyone` permission, OneDrive anonymous view link) and returns it. The grant stays until it is revoked on the provider.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**file_id** | **String** |  | [required] |
**account_id** | **String** | The connected Google or Microsoft account. | [required] |

### Return type

[**models::GetFileShareLink200Response**](getFileShareLink_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_files

> models::ListFiles200Response list_files(account_id, folder_id, q, cursor, limit)
List files in a folder or search the drive

Lists the children of `folderId` (the root by default), folders first.  With `q` and no `folderId` the whole drive is searched by name (on Google, every drive the app can see, shared drives included).  - The account must have been connected with `scopes=files` (412 `account_scope_missing` otherwise). - Cursors are opaque and provider-issued. - Google Drive returns only files Zernio created or the user picked (see the Files tag): an unpicked folder lists empty. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The connected Google or Microsoft account. | [required] |
**folder_id** | Option<**String**> | Provider folder id; omit for the root. |  |
**q** | Option<**String**> | Name search. |  |
**cursor** | Option<**String**> |  |  |
**limit** | Option<**i32**> |  |  |[default to 50]

### Return type

[**models::ListFiles200Response**](listFiles_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## trash_file

> models::TrashFile200Response trash_file(file_id, account_id)
Move a file to the trash

Drive trash or the OneDrive recycle bin; nothing is destroyed and the user can restore it on the provider.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**file_id** | **String** |  | [required] |
**account_id** | **String** | The connected Google or Microsoft account. | [required] |

### Return type

[**models::TrashFile200Response**](trashFile_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_file

> models::UploadFile201Response update_file(file_id, update_file_request)
Rename or move a file

`parentId` moves the item into another folder; `name` renames it. At least one is required.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**file_id** | **String** |  | [required] |
**update_file_request** | [**UpdateFileRequest**](UpdateFileRequest.md) |  | [required] |

### Return type

[**models::UploadFile201Response**](uploadFile_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## upload_file

> models::UploadFile201Response upload_file(upload_file_request)
Upload a file

Either `multipart/form-data` with the file under `file` plus `accountId`, `name` (defaults to the file name) and `parentId`, or JSON with a public `url` the file is fetched from (100 MB cap). Large files go through the provider's resumable upload.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**upload_file_request** | [**UploadFileRequest**](UploadFileRequest.md) |  | [required] |

### Return type

[**models::UploadFile201Response**](uploadFile_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json, multipart/form-data
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

