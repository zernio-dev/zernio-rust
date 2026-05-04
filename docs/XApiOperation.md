# XApiOperation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**operation** | Option<**String**> | Internal operation key. Matches keys in `xApiCallsByOperation`. | [optional]
**event_type** | Option<**String**> | Metronome `event_type` emitted when this operation runs. | [optional]
**display_name** | Option<**String**> | Human-readable label shown on Metronome invoices. | [optional]
**price_per_call_usd** | Option<**f64**> |  | [optional]
**price_per_call_cents** | Option<**f64**> | Per-call price in cents. Fractional values are intentional. | [optional]
**tier** | Option<**Tier**> | Which aggregate price tier this operation falls into. (enum: x_api_005, x_api_010, x_api_015) | [optional]
**triggered_by** | Option<[**Vec<models::XApiOperationTriggeredByInner>**](XApiOperationTriggeredByInner.md)> | Zernio platform methods that emit this operation, with their metering rule. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


