# LinkedInPlatformData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**document_title** | Option<**String**> | Title displayed on LinkedIn document (PDF/carousel) posts. Required by LinkedIn for document posts. If omitted, falls back to the media item title, then the filename. | [optional]
**organization_urn** | Option<**String**> | Target LinkedIn Organization URN (e.g. \"urn:li:organization:123456789\"). If omitted, uses the default org. Use GET /v1/accounts/{id}/linkedin-organizations to list orgs. | [optional]
**first_comment** | Option<**String**> | Optional first comment to add after the post is created | [optional]
**disable_link_preview** | Option<**bool**> | Set to true to disable automatic link previews for URLs in the post content (default is false) | [optional]
**reshare_url** | Option<**String**> | LinkedIn post link to repost (use the post's \"Copy link to post\" action), or a urn:li:share / urn:li:ugcPost / urn:li:groupPost URN. The published post is always a reshare authored by your account with the original embedded underneath: with content your text is the commentary (LinkedIn's \"repost with your thoughts\"), and with no content it publishes as a text-free reshare. Note that a text-free reshare is NOT LinkedIn's one-click \"Repost\" (the feed treatment where the original author stays the author); LinkedIn's API exposes no way to create that, so the post still appears authored by you with the original embedded. Mutually exclusive with media. Works on personal profiles and organization pages. | [optional]
**geo_restriction** | Option<[**models::GeoRestriction**](GeoRestriction.md)> |  | [optional]
**poll** | Option<[**models::LinkedInPlatformDataPoll**](LinkedInPlatformDataPoll.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


