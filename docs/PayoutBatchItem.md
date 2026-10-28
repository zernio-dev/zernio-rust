# PayoutBatchItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**participant_id** | **String** |  | 
**creator** | [**models::PayoutBatchItemCreator**](PayoutBatchItemCreator.md) |  | 
**amount_cents** | **i32** | What the creator receives, in full. | 
**fee_cents** | **i32** | Zernio fee on top: 4% with a 50 cent minimum. | 
**total_cents** | **i32** | amountCents plus feeCents. | 
**status** | **Status** | `skipped`: not paid because payout setup was not finished, or the card payment never completed; the amount is payable again. `failed`: Stripe refused the transfer; the amount is payable again. (enum: pending, paid, failed, skipped) | 
**failure_reason** | Option<**String**> | Why the item was not paid, in plain words. | 
**transfer_id** | Option<**String**> | The treasury transfer that paid this item. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


