# WebhookPayloadBalanceChargedTopup

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | The top-up id, as in GET /v1/balance (`recentTopups`) and its invoice and receipt endpoints. | 
**trigger** | **Trigger** | `manual`: someone topped up in Billing or through the API. `auto_top_up`: the auto top-up rule charged the card. (enum: manual, auto_top_up) | 
**amount_cents** | **i32** | Added to the balance, in USD cents. | 
**tax_cents** | **i32** | VAT charged on top, in USD cents (0 when none applies). | 
**charged_cents** | **i32** | What the card was charged, in USD cents: amount plus tax. | 
**currency** | **Currency** |  (enum: usd) | 
**card** | [**models::WebhookPayloadBalanceChargedTopupCard**](WebhookPayloadBalanceChargedTopupCard.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


