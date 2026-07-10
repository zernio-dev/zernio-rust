# UsageMetering

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**supported** | Option<**bool**> | False for legacy Stripe accounts (no Metronome invoice to split); `days` and `totals` are then empty/zero. | [optional]
**granularity** | Option<**Granularity**> |  (enum: day, month, total) | [optional]
**days** | Option<[**Vec<models::UsageMeteringDaysInner>**](UsageMeteringDaysInner.md)> | One row per bucket. Empty when `granularity=total`. `date` is a UTC date (month buckets use the 1st). | [optional]
**totals** | Option<[**models::UsageMeteringTotals**](UsageMeteringTotals.md)> |  | [optional]
**line_items** | Option<[**Vec<models::UsageMeteringLineItemsInner>**](UsageMeteringLineItemsInner.md)> | Per-invoice-line-item rows (largest spend first) for a detailed breakdown. | [optional]
**peaks** | Option<[**models::UsageMeteringPeaks**](UsageMeteringPeaks.md)> |  | [optional]
**call_usage** | Option<[**models::UsageMeteringCallUsage**](UsageMeteringCallUsage.md)> |  | [optional]
**period** | Option<[**models::UsageMeteringPeriod**](UsageMeteringPeriod.md)> |  | [optional]
**tax** | Option<[**models::UsageMeteringTax**](UsageMeteringTax.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


