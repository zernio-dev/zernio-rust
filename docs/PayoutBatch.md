# PayoutBatch

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**campaign_id** | Option<**String**> |  | 
**status** | **Status** | `awaiting_payment` until the card payment completes; `paying` while transfers go out; then `paid`, `partially_failed` (some items failed or were skipped), `failed` (none paid) or `expired` (the Checkout expired unpaid, every amount is payable again). (enum: awaiting_payment, paying, paid, partially_failed, failed, expired) | 
**method** | **Method** |  (enum: card) | 
**amount_cents** | **i32** | Total the creators receive. | 
**fee_cents** | **i32** | Total Zernio fee. | 
**total_cents** | **i32** | The card charge: amountCents plus feeCents. | 
**items** | [**Vec<models::PayoutBatchItem>**](PayoutBatchItem.md) |  | 
**paid_at** | Option<**String**> |  | 
**finished_at** | Option<**String**> |  | 
**created_at** | **String** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


