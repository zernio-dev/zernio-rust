# CreateProfileRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** |  | 
**description** | Option<**String**> |  | [optional]
**color** | Option<**String**> |  | [optional]
**timezone** | Option<**String**> | IANA timezone new posts on this profile use when they name no `timezone`. Omit to keep UTC. An unknown name returns 400. | [optional]
**external_id** | Option<**String**> | Your own identifier for this profile, typically the id of the tenant or client it serves in your system (1 to 255 characters, trimmed). Unique among the profiles of the user who owns the profile: a duplicate returns 409 profile_external_id_conflict. Look a profile up by it with GET /v1/profiles?externalId=. | [optional]
**content_retention** | Option<**ContentRetention**> | Set `none` to create the profile with zero content retention, so nothing of its accounts is stored from the first sync. Only the team owner can, with a session or a full-access key; anyone else gets 403. (enum: standard, none) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


