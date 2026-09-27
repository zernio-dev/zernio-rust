# WebhookPayloadTest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Stable webhook event ID: the dedupe key, also sent as the X-Zernio-Event-Id header and identical on every retry and redelivery. It identifies the event only, never an account or other resource. | 
**event** | **Event** |  (enum: webhook.test) | 
**message** | **String** | Human-readable test message | 
**timestamp** | **String** | UTC time at which Zernio generated this test event (set once when the payload is built). Test fires are sent synchronously as a single attempt; a later redelivery of this event keeps the original value. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


