# GetVoiceCallEstimate200ResponseBreakdown

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**telnyx_cost_usd** | Option<**f64**> |  | [optional]
**recording_cost_usd** | Option<**f64**> |  | [optional]
**transcription_cost_usd** | Option<**f64**> |  | [optional]
**branded_call_usd** | Option<**f64**> | Branded Calling surcharge, 0 unless `from` is a verified branded number calling a US destination. | [optional]
**billable_cost_usd** | Option<**f64**> | What Zernio bills for the call. | [optional]
**total_cost_usd** | Option<**f64**> | Equals billableCostUSD (no separate Meta bill on PSTN); kept for shape parity with the WhatsApp estimate. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


