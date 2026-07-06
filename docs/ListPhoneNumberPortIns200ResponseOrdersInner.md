# ListPhoneNumberPortIns200ResponseOrdersInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**status** | Option<**Status**> |  (enum: draft, pending, foc_confirmed, ported, exception, cancelled) | [optional]
**telnyx_status_value** | Option<**String**> | Raw carrier status string. | [optional]
**phone_numbers** | Option<**Vec<String>**> |  | [optional]
**fast_port_eligible** | Option<**bool**> |  | [optional]
**foc_datetime_requested** | Option<**String**> |  | [optional]
**foc_datetime_actual** | Option<**String**> |  | [optional]
**decline_reason** | Option<**String**> |  | [optional]
**submitted_at** | Option<**String**> |  | [optional]
**ported_at** | Option<**String**> |  | [optional]
**created_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


