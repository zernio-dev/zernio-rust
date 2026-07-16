# UsageMeteringTax

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tax_usd** | Option<**f64**> | Estimated tax in USD, added on top of `totals.total`. | [optional]
**rate_percent** | Option<**f64**> | Combined rate percentage, e.g. 21. | [optional]
**jurisdiction_label** | Option<**String**> | Human jurisdiction label, e.g. \"ES VAT\" or \"WA sales tax\". | [optional]
**reverse_charge** | Option<**bool**> | True for EU/UK B2B reverse charge (0 tax added by design). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


