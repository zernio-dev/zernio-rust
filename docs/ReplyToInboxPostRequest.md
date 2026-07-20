# ReplyToInboxPostRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** |  | 
**message** | **String** |  | 
**attachment_url** | Option<**String**> | (Facebook only) URL of an image to attach, publishing a photo comment alongside the text. The URL must be publicly accessible so Meta can fetch it. Returns 400 for other platforms. | [optional]
**comment_id** | Option<**String**> | Reply to specific comment (optional) | [optional]
**parent_cid** | Option<**String**> | (Bluesky only) Parent content identifier | [optional]
**root_uri** | Option<**String**> | (Bluesky only) Root post URI | [optional]
**root_cid** | Option<**String**> | (Bluesky only) Root post CID | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


