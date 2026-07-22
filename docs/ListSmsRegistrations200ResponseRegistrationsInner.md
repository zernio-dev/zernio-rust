# ListSmsRegistrations200ResponseRegistrationsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**registration_type** | Option<**RegistrationType**> |  (enum: standard_10dlc, sole_prop_10dlc, toll_free) | [optional]
**display_name** | Option<**String**> |  | [optional]
**status** | Option<**Status**> | requested/changes_requested = pre-submission review states; customers see them as pending / needs changes. (enum: pending, approved, rejected, requested, changes_requested, deactivated) | [optional]
**brand_status** | Option<**String**> | Carrier-registry brand status (e.g. VERIFIED). | [optional]
**campaign_status** | Option<**String**> |  | [optional]
**brand_id** | Option<**String**> | TCR brand id, useful when referencing the brand in carrier support threads. | [optional]
**campaign_id** | Option<**String**> | TCR campaign id. | [optional]
**decline_reason** | Option<**String**> |  | [optional]
**tf_action_required_at** | Option<**String**> | Toll-free only: when the carrier requested changes (\"Waiting For Customer\"). The request must be resubmitted within 7 days of this timestamp or it expires. | [optional]
**phone_numbers** | Option<**Vec<String>**> |  | [optional]
**awaiting_otp** | Option<**bool**> | Sole-prop 10DLC only; the OTP step is still pending. | [optional]
**trust_score** | Option<**f64**> | Carrier-assigned brand trust score; drives throughput. | [optional]
**throughput** | Option<[**models::ListSmsRegistrations200ResponseRegistrationsInnerThroughput**](ListSmsRegistrations200ResponseRegistrationsInnerThroughput.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


