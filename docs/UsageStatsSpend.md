# UsageStatsSpend

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**current_period_cents** | Option<**i32**> | Total current-period spend in cents (all products combined). | [optional]
**credits_remaining_cents** | Option<**i32**> | Free-tier credit remaining in cents. Applied before any charge. | [optional]
**x_spend_cents** | Option<**i32**> | Current-period X/Twitter API spend in cents, summed from `xApiCallsByOperation` × per-operation prices. Tier-agnostic (covers every price including the $0.200 URL tier). Rounded up for conservative enforcement against `xSpendLimitCents`.  | [optional]
**x_spend_limit_cents** | Option<**i32**> | Monthly X spend cap set by the account owner, or null if no cap. When current X spend hits this cap, analytics and inbox sync are auto-paused for X accounts. Publishing is never blocked by this cap.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


