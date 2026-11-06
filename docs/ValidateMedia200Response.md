# ValidateMedia200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**valid** | Option<**bool**> |  | [optional]
**url** | Option<**String**> |  | [optional]
**error** | Option<**String**> | Error message if valid is false | [optional]
**code** | Option<**Code**> | Stable reason when valid is false. MEDIA_UNDECODABLE: the bytes are not a valid image, video or PDF. MEDIA_URL_UNREACHABLE: HTTP error, timeout, network failure, or a web page served instead of the file. MEDIA_URL_NOT_ALLOWED: not a public HTTP(S) URL. (enum: MEDIA_UNDECODABLE, MEDIA_URL_UNREACHABLE, MEDIA_URL_NOT_ALLOWED) | [optional]
**content_type** | Option<**String**> | Content-Type header the server sent (may disagree with the detected format) | [optional]
**size** | Option<**i32**> | File size in bytes | [optional]
**size_formatted** | Option<**String**> |  | [optional]
**r#type** | Option<**Type**> | Detected from the file bytes (enum: image, video, document) | [optional]
**format** | Option<**String**> | Detected format (jpeg, png, webp, gif, heif, mp4, mov, webm, pdf, ...) | [optional]
**width** | Option<**i32**> | Image width in pixels (images only) | [optional]
**height** | Option<**i32**> | Image height in pixels (images only) | [optional]
**inspection** | Option<**Inspection**> | How deeply the content was verified. decoded: every pixel decoded. header: file signature and header verified (videos, PDFs, HEIC/AVIF, images over 32 MB). (enum: decoded, header) | [optional]
**platform_limits** | Option<[**std::collections::HashMap<String, models::ValidateMedia200ResponsePlatformLimitsValue>**](ValidateMedia200ResponsePlatformLimitsValue.md)> | Per-platform size limit comparison (only present when size and type are known) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


