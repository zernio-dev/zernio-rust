# WebhookPayloadCommerceOrder

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**test** | Option<**bool**> | Always true when present: only a sample sent by POST /v1/webhooks/test with an event carries it. Real deliveries never do. | [optional]
**id** | Option<**String**> |  | [optional]
**event** | Option<**Event**> |  (enum: commerce.order.created, commerce.order.updated, commerce.order.refunded) | [optional]
**timestamp** | Option<**String**> | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. | [optional]
**store** | Option<[**models::WebhookPayloadCommerceProductStore**](WebhookPayloadCommerceProductStore.md)> |  | [optional]
**resource** | Option<[**models::WebhookPayloadCommerceOrderResource**](WebhookPayloadCommerceOrderResource.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


