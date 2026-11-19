# GetVoiceCallEstimate200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**via** | Option<**Via**> |  (enum: trunk, voice) | [optional]
**destination_country** | Option<**String**> | ISO country of `to`. Isle of Man, Jersey and Guernsey numbers return IM, JE and GG. | [optional]
**line_type** | Option<**LineType**> | Line type of `to`. Where it is not `mobile` or `landline`, `perMinuteUsd` takes the dearer of the two. (enum: mobile, landline, fixed_line_or_mobile, other, unknown) | [optional]
**caller_id** | Option<**String**> | Caller ID the rates were picked for. Voice API estimates without `from` use your first calling number. | [optional]
**caller_country** | Option<**String**> |  | [optional]
**minutes** | Option<**i32**> |  | [optional]
**per_minute_usd** | Option<**f64**> | Billable cost per minute for `to`'s line type and the requested options. | [optional]
**billing_increment_seconds** | Option<[**models::GetVoiceCallEstimate200ResponseBillingIncrementSeconds**](GetVoiceCallEstimate200ResponseBillingIncrementSeconds.md)> |  | [optional]
**rates** | Option<[**models::GetVoiceCallEstimate200ResponseRates**](GetVoiceCallEstimate200ResponseRates.md)> |  | [optional]
**trunk** | Option<[**models::GetVoiceCallEstimate200ResponseTrunk**](GetVoiceCallEstimate200ResponseTrunk.md)> |  | [optional]
**breakdown** | Option<[**models::GetVoiceCallEstimate200ResponseBreakdown**](GetVoiceCallEstimate200ResponseBreakdown.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


