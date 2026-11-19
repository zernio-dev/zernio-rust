# WebhookPayloadBillingPublishingBlocked

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Stable webhook event ID: the dedupe key, also sent as the X-Zernio-Event-Id header and identical on every retry and redelivery. It identifies the event only, never an account or other resource. | 
**test** | Option<**bool**> | Always true when present: only a sample sent by POST /v1/webhooks/test with an event carries it. Real deliveries never do. | [optional]
**event** | **Event** |  (enum: billing.publishing_blocked) | 
**billing** | [**models::WebhookPayloadBillingPublishingBlockedBilling**](WebhookPayloadBillingPublishingBlockedBilling.md) |  | 
**billing_url** | **String** | Dashboard page where the owner pays or replaces the card. | 
**timestamp** | **String** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


