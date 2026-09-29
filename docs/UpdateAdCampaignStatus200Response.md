# UpdateAdCampaignStatus200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | Option<**Status**> | The campaign's delivery status derived from its switch as read back (`paused` when the switch is off). Echoes the request when the platform could not be read. (enum: active, paused) | [optional]
**platform_campaign_status** | Option<**String**> | The campaign's own switch as read back from the platform, in the raw platform vocabulary (Meta effective_status, TikTok ENABLE / DISABLE, Google ENABLED / PAUSED, ChatGPT (OpenAI) status). Null when the platform could not be read, which is always the case on Pinterest, LinkedIn and X (no single-campaign read). | [optional]
**status_read_at** | Option<**String**> | When the switch was read back. Null when it could not be read. | [optional]
**updated** | Option<**Updated**> | 1 when the campaign's switch was written. (enum: 0, 1) | [optional]
**skipped** | Option<**Skipped**> | 1 when a live read showed the campaign already in the requested state, so nothing was written. (enum: 0, 1) | [optional]
**skipped_reasons** | Option<**Vec<String>**> | Why the write was skipped, for example \"Campaign already switched off\". | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


