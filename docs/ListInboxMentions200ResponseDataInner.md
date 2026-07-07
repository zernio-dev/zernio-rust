# ListInboxMentions200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Mention document ID | [optional]
**platform** | Option<**Platform**> |  (enum: linkedin) | [optional]
**account_id** | Option<**String**> |  | [optional]
**account_username** | Option<**String**> |  | [optional]
**content** | Option<**String**> | Text of the post that mentioned you | [optional]
**permalink** | Option<**String**> | URL to the source post on LinkedIn | [optional]
**author_urn** | Option<**String**> | LinkedIn URN of the person who mentioned you | [optional]
**author_name** | Option<**String**> | Display name of the author, resolved from authorUrn. Null when LinkedIn does not allow resolving the profile. | [optional]
**author_username** | Option<**String**> | LinkedIn vanity name of the author (the slug in their profile URL) | [optional]
**author_picture** | Option<**String**> | Profile picture URL of the author. LinkedIn CDN URLs expire after some time, so fetch promptly rather than storing long-term. | [optional]
**organizational_entity** | Option<**String**> | URN of the organization that was mentioned | [optional]
**published_at** | Option<**String**> |  | [optional]
**created_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


