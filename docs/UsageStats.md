# UsageStats

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**billing_system** | Option<**BillingSystem**> | Which billing system the account is on. Shape of `usage`/`spend` differs. (enum: stripe, metronome) | [optional]
**plan_name** | Option<**String**> |  | [optional]
**billing_period** | Option<**BillingPeriod**> |  (enum: monthly, yearly) | [optional]
**signup_date** | Option<**String**> |  | [optional]
**billing_anchor_day** | Option<**i32**> | Day of month (1-31) when the billing cycle resets | [optional]
**has_access** | Option<**bool**> | True if the account is in good standing. False for past-due/unpaid/paused subscriptions. | [optional]
**customer_id** | Option<**String**> | Stripe customer ID, when present. | [optional]
**is_invited_user** | Option<**bool**> | True if this is a team member; limits/usage reflect the account owner. | [optional]
**auto_upgrade_enabled** | Option<**bool**> | Stripe-only. Always false for Metronome users. | [optional]
**limits** | Option<[**models::UsageStatsLimits**](UsageStatsLimits.md)> |  | [optional]
**usage** | Option<[**models::UsageStatsUsage**](UsageStatsUsage.md)> |  | [optional]
**spend** | Option<[**models::UsageStatsSpend**](UsageStatsSpend.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


