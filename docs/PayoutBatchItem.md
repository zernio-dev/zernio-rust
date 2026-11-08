# PayoutBatchItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**participant_id** | **String** |  | 
**creator** | [**models::PayoutBatchItemCreator**](PayoutBatchItemCreator.md) |  | 
**amount_cents** | **i32** | What the creator receives, in full. | 
**fee_cents** | **i32** | Zernio fee on top: 4%, 50 cents minimum per payout. | 
**total_cents** | **i32** | amountCents plus feeCents. | 
**status** | **Status** | `skipped`: payout setup not finished, or the card payment never completed. `failed`: Stripe refused the transfer. `refunded`: failed or skipped after the card hold; its payout, fee and VAT on the fee went back to the card through a credit note. The amount is payable again in every case. (enum: pending, paid, failed, skipped, refunded) | 
**failure_reason** | Option<**String**> | Why the item was not paid, in plain words. | 
**transfer_id** | Option<**String**> | The treasury transfer that paid this item. | 
**refunded_cents** | Option<**i32**> | What went back to the card for a `refunded` item: payout, fee and VAT on the fee. Null otherwise. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


