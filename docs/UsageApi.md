# \UsageApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_billing**](UsageApi.md#get_billing) | **GET** /v1/billing | Account billing snapshot (plan, cycle, balance, caps, status)
[**get_calls_usage**](UsageApi.md#get_calls_usage) | **GET** /v1/usage/calls | Calling usage and cost
[**get_sms_usage**](UsageApi.md#get_sms_usage) | **GET** /v1/usage/sms | SMS usage (volumes)
[**get_usage**](UsageApi.md#get_usage) | **GET** /v1/usage | Usage snapshot (default) or billed-spend metering (with params)
[**get_usage_stats**](UsageApi.md#get_usage_stats) | **GET** /v1/usage-stats | Get plan and usage snapshot (plan, limits, payment status)
[**get_x_api_pricing**](UsageApi.md#get_x_api_pricing) | **GET** /v1/billing/x-pricing | Get X/Twitter API pricing table



## get_billing

> models::BillingSnapshot get_billing()
Account billing snapshot (plan, cycle, balance, caps, status)

The billing \"wallet/statement\" view: current plan, billing cycle, accrued balance + remaining credits this period, spend caps, and payment / access status. This is the billing half of the legacy `/v1/usage-stats` snapshot — the per-product consumption half is metering and lives on `GET /v1/usage`.  Usage-based (Metronome) accounts get a populated `balance`; legacy Stripe accounts get `balance: null` plus a deprecated `legacy.limits` block and, when payment-blocked, `status.openInvoiceUrl` / `status.declineReason`. 

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::BillingSnapshot**](BillingSnapshot.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_calls_usage

> models::GetCallsUsage200Response get_calls_usage(since, until, channel, number, group_by)
Calling usage and cost

Aggregated calling usage across your numbers, both channels (WhatsApp Business Calling + regular phone/PSTN): call counts, answered counts, minutes, and cost. Use it for cost visibility or to rebill your own customers per number.  Costs come from each call's billing snapshot, so this endpoint always agrees with the invoice: `billableUSD` is what Zernio bills; `metaUSD` is the WhatsApp per-minute charge Meta bills directly to your WABA (display only, never billed by Zernio).  Optional `groupBy` returns a breakdown by UTC day, by your number, or by channel. Defaults to the last 30 days. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**since** | Option<**String**> | Start of the window (inclusive). Default 30 days before `until`. |  |
**until** | Option<**String**> | End of the window (exclusive). Default now. |  |
**channel** | Option<**String**> |  |  |
**number** | Option<**String**> | Scope to calls involving this number (typically one of YOUR numbers). E.164, leading + optional. |  |
**group_by** | Option<**String**> |  |  |

### Return type

[**models::GetCallsUsage200Response**](getCallsUsage_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_sms_usage

> models::GetSmsUsage200Response get_sms_usage(since, until, number, group_by)
SMS usage (volumes)

Aggregated SMS/MMS volumes across your numbers: sent, received, and total message counts, with an optional breakdown by UTC day or by number. Defaults to the last 30 days.  Volumes only, deliberately: SMS cost is carrier-rated asynchronously and billed to your invoice, so per-message cost is not available here. Calling usage (GET /v1/usage/calls) does include billable cost. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**since** | Option<**String**> | Start of the window (inclusive). Default 30 days before `until`. |  |
**until** | Option<**String**> | End of the window (exclusive). Default now. |  |
**number** | Option<**String**> | Scope to one of YOUR SMS-enabled numbers (E.164, leading + optional). |  |
**group_by** | Option<**String**> |  |  |

### Return type

[**models::GetSmsUsage200Response**](getSmsUsage_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_usage

> models::GetUsage200Response get_usage(reconcile, range, from, to, granularity)
Usage snapshot (default) or billed-spend metering (with params)

Dual-mode endpoint, selected by query params — fully backward compatible:  **Without metering params (the default):** the plan / quota / usage snapshot — plan name, billing period, limits, usage counts, access state. Identical to `GET /v1/usage-stats`. Existing integrations keep working unchanged.  **With `range`, `granularity`, `from`, or `to`:** usage METERING — billed spend (USD) by product family (`accounts`, `numbers`, `calls`, `sms`, `dlc`, `xApi`, `credits`, `other`) over the window, at `day` / `month` / `total` granularity, from Metronome's invoice breakdown (the CHARGE view — always reconciles with what gets billed). Also served at `GET /v1/usage/daily`. Usage-based accounts only — legacy Stripe accounts get `{ \"supported\": false, \"days\": [] }`.  For per-domain consumption *volumes* use `GET /v1/usage/calls` and `GET /v1/usage/sms`. For the billing statement (balance, credits, caps, payment status) use `GET /v1/billing`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**reconcile** | Option<**bool**> | Snapshot mode only. For Stripe subscription users, `true` forces a subscription reconciliation pass even when cached plan data looks complete.  |  |
**range** | Option<**String**> | Window to report. `cycle` / `prev-cycle` resolve to the customer's real billing-period bounds (falling back to a trailing 30 days when no invoice exists yet); `7d`…`12mo` are trailing windows; `custom` uses `from` / `to`.  |  |[default to cycle]
**from** | Option<**String**> | Inclusive start (UTC date). Required when `range=custom`. |  |
**to** | Option<**String**> | Inclusive end (UTC date). Required when `range=custom`. Max span 366 days. |  |
**granularity** | Option<**String**> | Bucketing of the `days` series: `day` (one row per UTC day), `month` (one row per calendar month, dated to the 1st), or `total` (no series — read `totals`). Does not affect `totals`.  |  |[default to day]

### Return type

[**models::GetUsage200Response**](getUsage_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_usage_stats

> models::UsageStats get_usage_stats(reconcile)
Get plan and usage snapshot (plan, limits, payment status)

The plan / quota / payment-status snapshot: current plan name, billing period, plan limits, usage counts, and access state. Identical to a bare `GET /v1/usage` call (this path is its deprecated alias). For billed spend by product, call `GET /v1/usage` with `range` / `granularity` params. The statement view (balance, credits, caps, payment status) lives at `GET /v1/billing`.  The response shape depends on the account's `billingSystem`:   * Stripe users: per-period `usage.uploads` / `usage.profiles` counters.   * Metronome (usage-based) users: `usage.connectedAccounts`,     `usage.xApiCallsByOperation` (per-operation X API call counts —     resolve keys via `GET /v1/billing/x-pricing`), plus a `spend`     block with `currentPeriodCents`, `xSpendCents`, and     `xSpendLimitCents`. The legacy `usage.xApiCalls` 3-tier     aggregate is still emitted for back-compat but excludes the     $0.200 URL tier and any future tiers — new clients should     consume `xApiCallsByOperation` only. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**reconcile** | Option<**bool**> | For Stripe subscription users, `true` forces a subscription reconciliation pass even when cached plan data looks complete. Omit the parameter, or pass `false`, to use the default first-time-only reconciliation behavior. Invalid boolean values are rejected.  |  |

### Return type

[**models::UsageStats**](UsageStats.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_x_api_pricing

> models::XApiPricing get_x_api_pricing()
Get X/Twitter API pricing table

Returns Zernio's canonical X/Twitter API pricing table. Each X action has its own Metronome product and its own rate, and Zernio passes X API costs through at exact rates with zero markup.  The response is identical for every authenticated user (pricing is universal), so it is safe to cache on the client for the duration of a billing period.  To compute your own per-operation spend, pair this endpoint with `GET /v1/usage-stats` — that endpoint returns `usage.xApiCallsByOperation` keyed by the same `operation` field you get here. 

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::XApiPricing**](XApiPricing.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

