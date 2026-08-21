# CreateStandaloneAdRequestVideo

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | Option<**String**> | Public URL of the video. Meta: uploaded via chunked transfer on /act_X/advideos, then the request blocks on Meta's transcoding until status.video_status === 'ready'. LinkedIn: uploaded via the Videos API (multipart), then the request blocks until LinkedIn finishes transcoding (status AVAILABLE) — short clips take ~10-30s. Provide either `url` or `id`. | [optional]
**id** | Option<**String**> | Meta only. Reuse a video ALREADY uploaded to this ad account instead of re-uploading the file: pass the `videoId` returned by a previous create. Wins over `url`, so N ads that differ only in copy share one upload (`existingCreativeId` only covers the identical-copy case). Provide either `url` or `id`. | [optional]
**thumbnail_url** | Option<**String**> | Public URL of a still-image thumbnail for the video. OPTIONAL: when omitted on Meta, the poster is auto-generated from Meta's own preferred video thumbnail (the same candidates Ads Manager shows), so video ads usually publish without supplying one. When Meta produces no candidate the request fails with a 502 platform_error (reason: video_thumbnail_unavailable) — retry, or supply this field. Provide it to control the poster frame exactly (uploaded as an ad image and referenced in object_story_spec.video_data). Ignored by LinkedIn (auto-generated poster frame). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


