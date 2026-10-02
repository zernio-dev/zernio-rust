# CampaignAnalyticsResponseCampaign

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**platform** | Option<**String**> |  | [optional]
**status** | Option<**String**> | The platform's own campaign status in its vocabulary (Google ENABLED / PAUSED / REMOVED, Meta ACTIVE / PAUSED, ...), the same value as platformCampaignStatus on /v1/ads/campaigns and /v1/ads/tree. For a campaign synced before that value was stored it falls back to an active child ad's status, else the newest ad's. | [optional]
**budget** | Option<[**models::AdCampaignBudget**](AdCampaignBudget.md)> |  | [optional]
**currency** | Option<**String**> | ISO 4217 code of the ad account (e.g. USD, THB). All money values in `summary` and `daily` are in this currency. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


