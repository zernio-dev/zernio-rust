# CreateTopupRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**amount_cents** | **i32** | Amount to charge and credit to your balance, in cents: $5 to $100,000. No card fee. | 
**method** | **Method** | Only card is available. bank_transfer returns 400 \"Bank transfers are not available yet.\" (enum: card, bank_transfer) | 
**payment_method_id** | Option<**String**> | A saved card of the billing owner's (`pm_...`). Defaults to the default payment method. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


