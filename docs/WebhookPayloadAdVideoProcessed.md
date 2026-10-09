# WebhookPayloadAdVideoProcessed

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Stable webhook event ID: the dedupe key, also sent as the X-Zernio-Event-Id header and identical on every retry and redelivery. | 
**test** | Option<**bool**> | Always true when present: only a sample sent by POST /v1/webhooks/test with an event carries it. Real deliveries never do. | [optional]
**event** | **Event** |  (enum: ad.video.processed) | 
**account** | [**models::WebhookPayloadAdVideoProcessedAccount**](WebhookPayloadAdVideoProcessedAccount.md) |  | 
**video** | [**models::WebhookPayloadAdVideoProcessedVideo**](WebhookPayloadAdVideoProcessedVideo.md) |  | 
**timestamp** | **String** | UTC time at which Zernio generated this event. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


