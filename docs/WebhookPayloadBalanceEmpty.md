# WebhookPayloadBalanceEmpty

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Stable webhook event ID: the dedupe key, also sent as the X-Zernio-Event-Id header and identical on every retry and redelivery. It identifies the event only, never an account or other resource. | 
**test** | Option<**bool**> | Always true when present: only a sample sent by POST /v1/webhooks/test with an event carries it. Real deliveries never do. | [optional]
**event** | **Event** |  (enum: balance.empty) | 
**balance** | [**models::WebhookPayloadBalanceEmptyBalance**](WebhookPayloadBalanceEmptyBalance.md) |  | 
**code** | **Code** | The 402 code pay-per-use calls get until the balance is funded. `usage_limit_reached` when the auto top-up monthly limit is what keeps it at $0. (enum: insufficient_balance, usage_limit_reached) | 
**funding_url** | **String** | Dashboard link that opens the Add funds drawer in Billing. | 
**timestamp** | **String** | UTC time at which Zernio generated this event. Retries and redeliveries keep the original value. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


