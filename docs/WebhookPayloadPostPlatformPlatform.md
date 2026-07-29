# WebhookPayloadPostPlatformPlatform

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** | Platform name (e.g. `twitter`, `tiktok`, `instagram`). | 
**status** | **Status** | Terminal status this event fires on. Matches the event suffix. (enum: published, failed, deleted) | 
**platform_post_id** | Option<**String**> | Platform-native post id. Present on `published` and `deleted`, absent on `failed`. | [optional]
**published_url** | Option<**String**> | Public URL to the platform-side post. Present on `published` (when the platform exposes one and it is not a draft) and on `deleted` (when one was recorded at publish time). | [optional]
**error** | Option<**String**> | Error message from the platform. Present on `failed` only. | [optional]
**deleted_at** | Option<**String**> | When the platform-side deletion was detected by Zernio sync (ISO 8601). Present only on `post.platform.deleted`. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


