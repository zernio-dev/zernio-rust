# UpdateAdSetStatus200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | Option<**Status**> | The ad set's delivery status derived from the switches read back: `paused` when its own switch or its campaign's switch is off. Echoes the request when the platform could not be read. (enum: active, paused) | [optional]
**platform_ad_set_status** | Option<**String**> | The ad set's own switch as read back from the platform, in the raw platform vocabulary (Meta effective_status, TikTok ENABLE / DISABLE, Google ENABLED / PAUSED, LinkedIn and Pinterest ACTIVE / PAUSED, ChatGPT (OpenAI) status). Null when the platform could not be read, which is always the case on X. | [optional]
**platform_campaign_status** | Option<**String**> | The parent campaign's switch, read in the same call where the platform returns it, otherwise the stored value. | [optional]
**status_read_at** | Option<**String**> | When the ad set switch was read back. Null when it could not be read. | [optional]
**updated** | Option<**Updated**> | 1 when the ad set's switch was written. (enum: 0, 1) | [optional]
**skipped** | Option<**Skipped**> | 1 when a live read showed the ad set already in the requested state, so nothing was written. (enum: 0, 1) | [optional]
**skipped_reasons** | Option<**Vec<String>**> | Why the write was skipped, for example \"Ad set already switched off\". | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


