# PayoutBatch

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**campaign_id** | Option<**String**> |  | 
**status** | **Status** | `awaiting_payment` until the card charge succeeds (3D Secure included); `paying` during the 7-day card hold and while transfers go out; then `paid`, `partially_failed` (some items failed or were skipped), `failed` (the card was declined, or none paid) or `expired` (the payment was cancelled unpaid, every amount is payable again). (enum: awaiting_payment, paying, paid, partially_failed, failed, expired) | 
**method** | **Method** |  (enum: card) | 
**amount_cents** | **i32** | Total the creators receive. | 
**fee_cents** | **i32** | Total Zernio fee. | 
**total_cents** | **i32** | amountCents plus feeCents. The card is charged this plus the VAT on the fee where it applies (see the batch invoice). | 
**items** | [**Vec<models::PayoutBatchItem>**](PayoutBatchItem.md) |  | 
**paid_at** | Option<**String**> |  | 
**releases_at** | Option<**String**> | When the 7-day card hold ends and the creators are paid. Null until the charge succeeds. | 
**finished_at** | Option<**String**> |  | 
**created_at** | **String** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


