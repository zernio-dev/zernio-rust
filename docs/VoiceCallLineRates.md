# VoiceCallLineRates

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**origination** | Option<**Origination**> | Caller-ID band the carrier rates this call with. `unknown_caller` (no caller ID) shows the dearest band. (enum: local, from_eea, non_surcharged, low_surcharged, high_surcharged, surcharged, default, unknown_caller) | [optional]
**per_minute_usd** | Option<**f64**> | The rate most of this line type's networks share. | [optional]
**min_per_minute_usd** | Option<**f64**> |  | [optional]
**max_per_minute_usd** | Option<**f64**> |  | [optional]
**networks** | Option<[**Vec<models::VoiceCallLineRatesNetworksInner>**](VoiceCallLineRatesNetworksInner.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


