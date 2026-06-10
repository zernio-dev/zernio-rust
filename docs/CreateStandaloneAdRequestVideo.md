# CreateStandaloneAdRequestVideo

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **String** | Public URL of the video. Meta: uploaded via chunked transfer on /act_X/advideos, then the request blocks on Meta's transcoding until status.video_status === 'ready'. LinkedIn: uploaded via the Videos API (multipart), then the request blocks until LinkedIn finishes transcoding (status AVAILABLE) — short clips take ~10-30s. | 
**thumbnail_url** | Option<**String**> | Public URL of a still-image thumbnail for the video. OPTIONAL: when omitted on Meta, the poster is auto-generated from Meta's own preferred video thumbnail (the same candidates Ads Manager shows), so video ads publish without supplying one. Provide it to control the poster frame exactly (uploaded as an ad image and referenced in object_story_spec.video_data). Ignored by LinkedIn (auto-generated poster frame). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


