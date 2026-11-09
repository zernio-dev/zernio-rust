# ReplyToInboxPostRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** |  | 
**message** | **String** | Reply text. On LinkedIn, mention with @[https://www.linkedin.com/in/vanity] (resolved to LinkedIn's live name, same rules and errors as post content) or @[Name](urn:li:person|organization:ID); a hand-written name must match LinkedIn's exactly or it renders as plain text. | 
**attachment_url** | Option<**String**> | (Facebook only) URL of an image to attach, publishing a photo comment alongside the text. The URL must be publicly accessible so Meta can fetch it. Returns 400 for other platforms. | [optional]
**comment_id** | Option<**String**> | Reply to specific comment (optional) | [optional]
**mention_author** | Option<**bool**> | (LinkedIn only) When true, the reply starts with an @mention of the author of `commentId` (a member or a page), tagged with their URN and the name LinkedIn returns for them. Requires `commentId`.  - Returns 400 `platform_not_supported` on other platforms. - Returns 400 `linkedin_mention_name_unavailable` with `details.authorUrn` when LinkedIn does not return the author's name (for example a page the account does not administer); mention them in `message` as @[Name](urn) instead. - If LinkedIn rejects any mention in the reply, it is posted once more with every mention as plain text.  | [optional]
**parent_cid** | Option<**String**> | (Bluesky only) Parent content identifier | [optional]
**root_uri** | Option<**String**> | (Bluesky only) Root post URI | [optional]
**root_cid** | Option<**String**> | (Bluesky only) Root post CID | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


