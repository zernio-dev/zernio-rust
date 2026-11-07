# GetBalance200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**available_cents** | Option<**i32**> | Your balance. It goes negative after a dispute or refund of a spent top-up, or when pay-per-use already in flight lands past zero. The next top-up covers it. New payout batches are refused while it is negative. | [optional]
**promo_cents** | Option<**i32**> | Balance billing only (absent otherwise). Promotional and support credit Zernio added to your balance. Pay-per-use spends it before availableCents. It is never paid out to payees and is not part of availableCents. | [optional]
**payout_locked_cents** | Option<**i32**> | Always 0. The balance no longer pays creators, so none of it is locked from them. | [optional]
**payout_locks** | Option<[**Vec<models::GetBalance200ResponsePayoutLocksInner>**](GetBalance200ResponsePayoutLocksInner.md)> | Always empty. The balance no longer pays creators. | [optional]
**pending_cents** | Option<**i32**> | Card top-ups paid before 2026-10-29 that were held and are moving to availableCents (within the hour). Always 0 after that. | [optional]
**pending_releases** | Option<[**Vec<models::GetBalance200ResponsePendingReleasesInner>**](GetBalance200ResponsePendingReleasesInner.md)> | The held card top-ups behind pendingCents. | [optional]
**pending_topup_cents** | Option<**i32**> | Top-ups started but not paid yet. | [optional]
**currency** | Option<**Currency**> |  (enum: usd) | [optional]
**recent_topups** | Option<[**Vec<models::TreasuryTopup>**](TreasuryTopup.md)> |  | [optional]
**recent_credit_recharges** | Option<[**Vec<models::GetBalance200ResponseRecentCreditRechargesInner>**](GetBalance200ResponseRecentCreditRechargesInner.md)> | Balance billing only (absent otherwise). The 10 newest recharges paid from the account credit you held when you moved to the balance, newest first. Nothing was charged to your card and there is no invoice. The amount was added to promoCents with the credit's own expiry. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


