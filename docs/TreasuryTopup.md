# TreasuryTopup

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**method** | Option<**Method**> |  (enum: card, bank_transfer) | [optional]
**purpose** | Option<**Purpose**> | `balance` funds your balance; `payout_batch` is the card payment of one payout batch, which pays its creators directly. (enum: balance, payout_batch) | [optional]
**payout_batch** | Option<[**models::TreasuryTopupPayoutBatch**](TreasuryTopupPayoutBatch.md)> |  | [optional]
**fee_covered_by_zernio** | Option<**bool**> | True for a balance top-up (there is no card fee) and a `payout_batch` payment: Zernio pays the Stripe processing fee, so you are credited the whole charge. False on a top-up made before 2026-11-05. | [optional]
**amount_cents** | Option<**i32**> | The amount you asked for. A top-up credits exactly this and charges it plus tax (taxCents). Top-ups from 2026-11-02 to 2026-11-05 charged a card fee on top and credited what Stripe delivered; older ones charged this amount and credited it minus the fee. | [optional]
**fee_cents** | Option<**i32**> | Card fee you paid: 0 when Zernio covers it (feeCoveredByZernio). On an older top-up, the fee Stripe took once paid, the fee charged on top before, or null. | [optional]
**tax_cents** | Option<**i32**> | Tax charged on top of amountCents once paid (VAT where it applies, since 2026-11-05); 0 before payment, when reverse charged, outside the EU, and on older top-ups. | [optional]
**charged_cents** | Option<**i32**> | What your card was charged: amountCents plus taxCents, or amountCents plus the card fee on a top-up from 2026-11-02 to 2026-11-05. | [optional]
**stripe_fee_cents** | Option<**i32**> | feeCents once the top-up is paid; null before. Kept for older clients: read feeCents. | [optional]
**net_cents** | Option<**i32**> | Amount credited to your balance; null until paid. amountCents when feeCoveredByZernio; on an older top-up, what Stripe delivered. | [optional]
**status** | Option<**Status**> | `pending` until the card is charged (or 3D Secure is finished) and credited. `expired` means it ended unpaid: cancelled, or 3D Secure left unfinished for 30 minutes. Only `pending` counts toward pendingTopupCents. (enum: pending, succeeded, failed, expired) | [optional]
**created_at** | Option<**String**> |  | [optional]
**succeeded_at** | Option<**String**> |  | [optional]
**has_invoice** | Option<**bool**> | The paid payment has an invoice (getTopupInvoice): every balance top-up paid since 2026-11-05 (unless charged without one for a Stripe credit balance), and Checkout payments before 2026-10-29. Every paid payment has a card receipt (getTopupReceipt). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


