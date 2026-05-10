# UsageStatsUsage

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uploads** | Option<**i32**> | Stripe users only. Uploads consumed in the current period. | [optional]
**profiles** | Option<**i32**> | Stripe users only. Profiles currently owned. | [optional]
**last_reset** | Option<**String**> | Stripe users only. | [optional]
**connected_accounts** | Option<**i32**> | Metronome users only. Accounts currently connected across the team. | [optional]
**x_api_calls** | Option<[**models::UsageStatsUsageXApiCalls**](UsageStatsUsageXApiCalls.md)> |  | [optional]
**x_api_calls_by_operation** | Option<**std::collections::HashMap<String, i32>**> | Metronome users only. Per-operation X API call counts keyed by operation (e.g. `posts_read`, `content_create`, `content_create_with_url`). Resolve each key to price and metadata via `GET /v1/billing/x-pricing`. This is the canonical source — covers every price tier including the $0.200 URL tier that `xApiCalls` excludes.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


