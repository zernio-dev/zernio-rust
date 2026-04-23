# CreateStandaloneAdRequestVideo

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **String** | Public URL of the video. Uploaded to Meta via chunked transfer on /act_X/advideos; then the request blocks on Meta's transcoding until status.video_status === 'ready'. | 
**thumbnail_url** | **String** | Public URL of a still-image thumbnail for the video. Required by Meta on every video creative. Uploaded to Meta as an ad image and referenced as the thumbnail in object_story_spec.video_data. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


