# GetBalance200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**available_cents** | Option<**i32**> | Your balance, including card top-ups paid in the last 7 days (see payoutLockedCents). Negative after a dispute or refund of a top-up that was already spent; transfers are refused while it is negative. | [optional]
**payout_locked_cents** | Option<**i32**> | Part of availableCents from card top-ups charged in the last 7 days, net of refunds and disputes. Transfers to payees cannot use it yet; a transfer that needs it answers 409 `payout_funds_locked` with the day it can be sent. | [optional]
**payout_locks** | Option<[**Vec<models::GetBalance200ResponsePayoutLocksInner>**](GetBalance200ResponsePayoutLocksInner.md)> | The card top-ups behind payoutLockedCents, soonest first. | [optional]
**pending_cents** | Option<**i32**> | Card top-ups paid before 2026-10-29 that were held and are moving to availableCents (within the hour). Always 0 after that. | [optional]
**pending_releases** | Option<[**Vec<models::GetBalance200ResponsePendingReleasesInner>**](GetBalance200ResponsePendingReleasesInner.md)> | The held card top-ups behind pendingCents. | [optional]
**pending_topup_cents** | Option<**i32**> | Top-ups started but not paid yet. | [optional]
**currency** | Option<**Currency**> |  (enum: usd) | [optional]
**recent_topups** | Option<[**Vec<models::TreasuryTopup>**](TreasuryTopup.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


