# XApiPricing

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currency** | Option<**String**> |  | [optional]
**markup** | Option<**String**> | Always 0% — Zernio does not mark up X API rates. | [optional]
**source** | Option<**String**> |  | [optional]
**last_verified** | Option<[**String**](String.md)> | Date the prices were last verified against X's published rates. | [optional]
**tiers** | Option<[**Vec<models::XApiPricingTiersInner>**](XApiPricingTiersInner.md)> | Rollup of operations grouped by their per-call price. | [optional]
**operations** | Option<[**Vec<models::XApiOperation>**](XApiOperation.md)> | Flat list of every X operation Zernio can perform, with its rate. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


