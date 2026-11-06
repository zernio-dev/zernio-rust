# GetTopupInvoice200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **String** |  | 
**format** | **Format** |  (enum: pdf, page) | 
**pdf_url** | Option<**String**> | The invoice PDF. | 
**page_url** | Option<**String**> | The invoice's Stripe-hosted page. | 
**amount_cents** | **i32** | Amount added to your balance, as in the top-up list. | 
**tax_cents** | **i32** | Tax charged on top of amountCents. | 
**charged_cents** | **i32** | What the card was charged, tax included. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


