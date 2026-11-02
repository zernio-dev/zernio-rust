# CreateTopup201Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**topup_id** | **String** |  | 
**amount_cents** | **i32** | Credited to your balance once paid: exactly this when feeIsExact, else at least this. | 
**fee_cents** | **i32** | Card fee, charged on top of amountCents. | 
**charged_cents** | **i32** | What the card is charged: amountCents plus feeCents. | 
**fee_is_exact** | **bool** | True when feeCents is exactly Stripe's fee for this card. False when it is the region's highest rate, so Stripe may take less and the difference is added to your balance. | 
**status** | **Status** |  (enum: succeeded, processing, requires_action) | 
**client_secret** | Option<**String**> | PaymentIntent client secret for Stripe.js handleNextAction; set only when status is requires_action | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


