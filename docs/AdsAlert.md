# AdsAlert

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Stable for the same problem on the same entity. Pass it to POST /v1/ads/alerts/{alertId}/dismiss. | [optional]
**kind** | Option<**Kind**> |  (enum: ad_rejected, delivery_issue, payment, budget_limited, spend_no_results, connection_lost, sync_failing) | [optional]
**severity** | Option<**Severity**> |  (enum: error, warning, info) | [optional]
**title** | Option<**String**> |  | [optional]
**message** | Option<**String**> | What happened, in plain words. For a rejection or delivery issue, the platform's own reason when it gave one. | [optional]
**platform** | Option<**String**> |  | [optional]
**platform_ad_account_id** | Option<**String**> |  | [optional]
**entity** | Option<[**models::AdsAlertEntity**](AdsAlertEntity.md)> |  | [optional]
**ad_id** | Option<**String**> | The Zernio ad id when the entity is an ad, for GET /v1/ads/{adId}. | [optional]
**account_id** | Option<**String**> | The Zernio ads connection, on connection_lost and sync_failing alerts. | [optional]
**currency** | Option<**String**> |  | [optional]
**detected_at** | Option<**String**> |  | [optional]
**fix** | Option<[**models::AdsAlertFix**](AdsAlertFix.md)> |  | [optional]
**dismissed** | Option<**bool**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


