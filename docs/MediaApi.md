# \MediaApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_media_presigned_url**](MediaApi.md#get_media_presigned_url) | **POST** /v1/media/presign | Get upload URL



## get_media_presigned_url

> models::GetMediaPresignedUrl200Response get_media_presigned_url(get_media_presigned_url_request)
Get upload URL

Get a presigned URL to upload files directly to cloud storage (up to 5GB). Returns an uploadUrl and publicUrl. PUT your file to the uploadUrl, then use the publicUrl in your posts.  By default the file is written to temporary storage and auto-deletes 7 days after upload, so the publicUrl stops resolving once that window passes. Send `permanent: true` to write straight to permanent storage, which has no expiry: use it for anything that must stay reachable for longer, in particular cover and thumbnail images on posts scheduled more than a week out. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**get_media_presigned_url_request** | [**GetMediaPresignedUrlRequest**](GetMediaPresignedUrlRequest.md) |  | [required] |

### Return type

[**models::GetMediaPresignedUrl200Response**](getMediaPresignedUrl_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

