# TreasuryTopup

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**method** | Option<**Method**> |  (enum: card, bank_transfer) | [optional]
**purpose** | Option<**Purpose**> | `balance` funds your balance; `payout_batch` is the card payment of one payout batch, which pays its creators directly. (enum: balance, payout_batch) | [optional]
**payout_batch** | Option<[**models::TreasuryTopupPayoutBatch**](TreasuryTopupPayoutBatch.md)> |  | [optional]
**fee_covered_by_zernio** | Option<**bool**> | True for a `payout_batch` payment: Zernio pays the Stripe processing fee out of its transfer fee, so you are credited the whole charge. | [optional]
**amount_cents** | Option<**i32**> | Gross amount charged | [optional]
**stripe_fee_cents** | Option<**i32**> | Stripe processing fee you paid; null until Stripe reports it, 0 when Zernio covers it | [optional]
**net_cents** | Option<**i32**> | Amount credited to your balance: gross minus the Stripe fee, or the whole charge when Zernio covers the fee; null until Stripe reports it | [optional]
**status** | Option<**Status**> | `pending` until the card is charged (or 3D Secure is finished) and credited. `expired` means it ended unpaid: cancelled, or 3D Secure left unfinished for 30 minutes. Only `pending` counts toward pendingTopupCents. (enum: pending, succeeded, failed, expired) | [optional]
**created_at** | Option<**String**> |  | [optional]
**succeeded_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


