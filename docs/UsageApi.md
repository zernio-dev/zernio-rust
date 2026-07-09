# \UsageApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_calls_usage**](UsageApi.md#get_calls_usage) | **GET** /v1/usage/calls | Calling usage and cost
[**get_sms_usage**](UsageApi.md#get_sms_usage) | **GET** /v1/usage/sms | SMS usage (volumes)
[**get_usage**](UsageApi.md#get_usage) | **GET** /v1/usage | Get plan and usage snapshot
[**get_usage_stats**](UsageApi.md#get_usage_stats) | **GET** /v1/usage-stats | Get plan and usage stats
[**get_x_api_pricing**](UsageApi.md#get_x_api_pricing) | **GET** /v1/billing/x-pricing | Get X/Twitter API pricing table



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

> models::UsageStats get_usage(reconcile)
Get plan and usage snapshot

The usage hub: current plan name, billing period, plan limits, and usage counts, in one snapshot. For metered consumption over an arbitrary window with breakdowns (by day, by number), use the domain spokes: `GET /v1/usage/calls` and `GET /v1/usage/sms`.  The response shape depends on the account's `billingSystem`:   * Stripe users: per-period `usage.uploads` / `usage.profiles` counters.   * Metronome (usage-based) users: `usage.connectedAccounts`,     `usage.xApiCallsByOperation` (per-operation X API call counts —     resolve keys via `GET /v1/billing/x-pricing`), plus a `spend`     block with `currentPeriodCents`, `xSpendCents`, and     `xSpendLimitCents`. The legacy `usage.xApiCalls` 3-tier     aggregate is still emitted for back-compat but excludes the     $0.200 URL tier and any future tiers — new clients should     consume `xApiCallsByOperation` only. 

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


## get_usage_stats

> models::UsageStats get_usage_stats(reconcile)
Get plan and usage stats

Deprecated alias of `GET /v1/usage`; same contract. New integrations should use that path (the usage hub), with `GET /v1/usage/calls` and `GET /v1/usage/sms` for metered breakdowns.  Returns the current plan name, billing period, plan limits, and usage counts.  The response shape depends on the account's `billingSystem`:   * Stripe users: per-period `usage.uploads` / `usage.profiles` counters.   * Metronome (usage-based) users: `usage.connectedAccounts`,     `usage.xApiCallsByOperation` (per-operation X API call counts —     resolve keys via `GET /v1/billing/x-pricing`), plus a `spend`     block with `currentPeriodCents`, `xSpendCents`, and     `xSpendLimitCents`. The legacy `usage.xApiCalls` 3-tier     aggregate is still emitted for back-compat but excludes the     $0.200 URL tier and any future tiers — new clients should     consume `xApiCallsByOperation` only. 

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

