# CreateTopup201Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**topup_id** | **String** |  | 
**amount_cents** | **i32** | Charged and credited to your balance once paid. | 
**fee_cents** | **i32** | Always 0: there is no card fee. Kept for older clients. | 
**charged_cents** | **i32** | What the card is charged: amountCents. Kept for older clients. | 
**fee_is_exact** | **bool** | Always true. Kept for older clients. | 
**status** | **Status** |  (enum: succeeded, processing, requires_action) | 
**client_secret** | Option<**String**> | PaymentIntent client secret for Stripe.js handleNextAction; set only when status is requires_action | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


