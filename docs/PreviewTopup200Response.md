# PreviewTopup200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**amount_cents** | **i32** | Credited to your balance. | 
**tax_cents** | **i32** | Tax added on top (VAT where it applies). | 
**total_cents** | **i32** | What the card would be charged: amountCents + taxCents. | 
**tax_label** | Option<**String**> | The tax and its rate, for example \"VAT 21%\". Null when no tax is charged. | 
**reverse_charge** | **bool** | True for an EU business with a valid VAT id: no VAT, reverse charge. | 
**country** | Option<**String**> | Two-letter country the tax was placed in, from the billing address. Null when Stripe Tax returned no address. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


