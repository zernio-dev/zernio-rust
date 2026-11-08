# PreviewCampaignPayoutBatch200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**payout_count** | **i32** | Creators who would be paid. | 
**amount_cents** | **i32** | Total the creators receive. | 
**fee_cents** | **i32** | Zernio fee: 4%, 50 cents minimum per payout. | 
**tax_cents** | **i32** | VAT on the fee, 0 when none applies. | 
**total_cents** | **i32** | What the card would be charged: amountCents + feeCents + taxCents. | 
**tax_label** | Option<**String**> | For example \"VAT 21%\". Null when there is no tax. | 
**reverse_charge** | **bool** | The fee is reverse charged: you account for the VAT. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


