# CheckPhoneNumberPortability200ResponseResultsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**phone_number** | Option<**String**> |  | [optional]
**portable** | Option<**bool**> |  | [optional]
**fast_portable** | Option<**bool**> | Qualifies for the carrier's accelerated FastPort lane. | [optional]
**line_type** | Option<**String**> | Line type when known (mobile, landline, voip…). A US/CA mobile number requires the transfer PIN at submit. | [optional]
**country_code** | Option<**String**> | ISO country of the number — pass it to GET /v1/phone-numbers/port-in/requirements for international numbers. | [optional]
**phone_number_type** | Option<**String**> | Carrier number-type classification (local, mobile, national, toll_free…) — the numberType for the requirements endpoint. | [optional]
**not_portable_reason** | Option<**String**> | Carrier reason when not portable; null when portable. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


