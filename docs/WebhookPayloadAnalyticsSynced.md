# WebhookPayloadAnalyticsSynced

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Stable webhook event ID: the dedupe key, also sent as the X-Zernio-Event-Id header and identical on every retry and redelivery. It identifies the event only, never an account or other resource. | 
**event** | **Event** |  (enum: analytics.synced) | 
**account** | [**models::WebhookPayloadAnalyticsSyncedAccount**](WebhookPayloadAnalyticsSyncedAccount.md) |  | 
**sync** | [**models::WebhookPayloadAnalyticsSyncedSync**](WebhookPayloadAnalyticsSyncedSync.md) |  | 
**timestamp** | **String** | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


