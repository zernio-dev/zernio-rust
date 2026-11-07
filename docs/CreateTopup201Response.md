# CreateTopup201Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**topup_id** | **String** |  | 
**amount_cents** | **i32** | Credited to your balance once paid. | 
**tax_cents** | **i32** | Tax added on top of amountCents (VAT where it applies). 0 when reverse charged or outside the EU. | 
**total_cents** | **i32** | What the card is charged: amountCents + taxCents. | 
**tax_label** | Option<**String**> | The tax and its rate, for example \"VAT 21%\". Null when no tax is charged. | 
**reverse_charge** | **bool** | True for an EU business whose VAT id VIES confirms: no VAT is charged and the invoice says reverse charge (inversión del sujeto pasivo). | 
**fee_cents** | **i32** | Always 0: there is no card fee. Kept for older clients. | 
**charged_cents** | **i32** | Same as totalCents. Kept for older clients. | 
**fee_is_exact** | **bool** | Always true. Kept for older clients. | 
**status** | **Status** |  (enum: succeeded, processing, requires_action) | 
**client_secret** | Option<**String**> | PaymentIntent client secret for Stripe.js handleNextAction; set only when status is requires_action | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


