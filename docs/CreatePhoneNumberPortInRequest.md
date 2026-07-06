# CreatePhoneNumberPortInRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**phone_numbers** | **Vec<String>** | E.164 numbers to port in. | 
**end_user** | [**models::CreatePhoneNumberPortInRequestEndUser**](CreatePhoneNumberPortInRequestEndUser.md) |  | 
**loa_document_id** | **String** | Document id from POST /v1/phone-numbers/port-in/documents (kind=loa). | 
**invoice_document_id** | **String** | Document id from POST /v1/phone-numbers/port-in/documents (kind=invoice). | 
**foc_datetime_requested** | Option<**String**> | Requested port date; the carrier confirms the actual FOC later. | [optional]
**customer_reference** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


