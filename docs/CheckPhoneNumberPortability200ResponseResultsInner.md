# CheckPhoneNumberPortability200ResponseResultsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**phone_number** | Option<**String**> |  | [optional]
**portable** | Option<**bool**> |  | [optional]
**fast_portable** | Option<**bool**> | Qualifies for the carrier's accelerated FastPort lane. | [optional]
**messaging_capable** | Option<**bool**> | Whether texting can be enabled on the number once ported; null when the carrier does not say. | [optional]
**line_type** | Option<**String**> | Line type when known (mobile, landline, voip, toll-free, unknown). US/CA portable numbers only. A US/CA mobile number requires the transfer PIN at submit. | [optional]
**carrier_name** | Option<**String**> | The number's current carrier, when the lookup knows it. US/CA portable numbers only. | [optional]
**country_code** | Option<**String**> | ISO country of the number. Pass it to GET /v1/phone-numbers/port-in/requirements for international numbers. | [optional]
**phone_number_type** | Option<**String**> | Carrier number-type classification (local, mobile, national, toll_free...), the numberType for the requirements endpoint. | [optional]
**not_portable_reason** | Option<**String**> | Carrier reason when not portable; null when portable. | [optional]
**claim_id** | Option<**String**> | Keyless calls and claimLinks=true only, on portable results. Resolve it with GET /v1/phone-numbers/port-in/claims/{claimId}. Expires after 7 days. | [optional]
**claim_url** | Option<**String**> | Keyless calls and claimLinks=true only, on portable results. A signup link that lands on the dashboard's port form with this number filled in. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


