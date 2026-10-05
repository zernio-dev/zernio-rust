# GetAdVideoStatus200ResponseVideo

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**status** | **Status** |  (enum: processing, ready, error) | 
**platform_status** | Option<**String**> | Meta's raw status.video_status, forwarded verbatim. | 
**processing_progress** | Option<**i32**> | Meta's processing percentage when reported. | 
**error** | Option<**String**> | Meta's processing error when status is error. | 
**thumbnail_url** | Option<**String**> | Meta's auto-generated poster once ready, when Meta produced one. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


