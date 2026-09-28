# WebhookPayloadAccountAdsSyncFailed

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Stable webhook event ID: the dedupe key, also sent as the X-Zernio-Event-Id header and identical on every retry and redelivery. | 
**event** | **Event** |  (enum: account.ads.sync_failed) | 
**account** | [**models::WebhookAdsSyncAccount**](WebhookAdsSyncAccount.md) |  | 
**ad_account** | [**models::WebhookAdsSyncAdAccount**](WebhookAdsSyncAdAccount.md) |  | 
**sync** | [**models::WebhookPayloadAccountAdsSyncFailedSync**](WebhookPayloadAccountAdsSyncFailedSync.md) |  | 
**timestamp** | **String** | UTC time at which Zernio generated this event. Retries and redeliveries keep the original value. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


