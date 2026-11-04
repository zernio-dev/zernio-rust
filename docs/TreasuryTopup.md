# TreasuryTopup

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**method** | Option<**Method**> |  (enum: card, bank_transfer) | [optional]
**purpose** | Option<**Purpose**> | `balance` funds your balance; `payout_batch` is the card payment of one payout batch, which pays its creators directly. (enum: balance, payout_batch) | [optional]
**payout_batch** | Option<[**models::TreasuryTopupPayoutBatch**](TreasuryTopupPayoutBatch.md)> |  | [optional]
**fee_covered_by_zernio** | Option<**bool**> | True for a `payout_batch` payment: Zernio pays the Stripe processing fee out of its transfer fee, so you are credited the whole charge. | [optional]
**amount_cents** | Option<**i32**> | The amount you asked for. A top-up charges the card fee on top of it and credits what Stripe delivers, at least this amount. Older top-ups charged this amount and credited it minus the fee. | [optional]
**fee_cents** | Option<**i32**> | Card fee. Once paid, the fee Stripe took (chargedCents minus netCents). Before, the fee charged on top, or null on an older top-up. 0 when Zernio covers it (`payout_batch`). | [optional]
**charged_cents** | Option<**i32**> | What your card was charged: amountCents plus the card fee charged on top, or amountCents on an older top-up and on a `payout_batch` payment. | [optional]
**stripe_fee_cents** | Option<**i32**> | feeCents once the top-up is paid; null before. Kept for older clients: read feeCents. | [optional]
**net_cents** | Option<**i32**> | Amount credited to your balance, what Stripe delivered; null until paid. At least amountCents on a top-up that charged the fee on top, and amountCents on `payout_batch` payments. | [optional]
**status** | Option<**Status**> | `pending` until the card is charged (or 3D Secure is finished) and credited. `expired` means it ended unpaid: cancelled, or 3D Secure left unfinished for 30 minutes. Only `pending` counts toward pendingTopupCents. (enum: pending, succeeded, failed, expired) | [optional]
**created_at** | Option<**String**> |  | [optional]
**succeeded_at** | Option<**String**> |  | [optional]
**has_invoice** | Option<**bool**> | A Stripe invoice exists for this payment (Checkout payments). Every paid payment has a card receipt; see getTopupReceipt. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


