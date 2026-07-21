# CreatePhoneNumberPortInRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**phone_numbers** | **Vec<String>** | E.164 numbers to port in. | 
**end_user** | [**models::CreatePhoneNumberPortInRequestEndUser**](CreatePhoneNumberPortInRequestEndUser.md) |  | 
**loa_document_id** | **String** | Document id from POST /v1/phone-numbers/port-in/documents (kind=loa). | 
**invoice_document_id** | **String** | Document id from POST /v1/phone-numbers/port-in/documents (kind=invoice). | 
**foc_datetime_requested** | Option<**String**> | Requested port date; the carrier confirms the actual FOC later. US/CA default is one week out (shifted off weekends); international orders are scheduled into the carrier's next allowed porting window at or after this date. | [optional]
**customer_reference** | Option<**String**> |  | [optional]
**port_type** | Option<**PortType**> | Whether the losing account ports all its numbers (full) or keeps some (partial). (enum: full, partial) | [optional][default to Full]
**requirements** | Option<[**Vec<models::CreatePhoneNumberPortInRequestRequirementsInner>**](CreatePhoneNumberPortInRequestRequirementsInner.md)> | Country-specific requirement values for international ports (from GET /v1/phone-numbers/port-in/requirements). Not needed for US/CA. The LOA and invoice requirements are satisfied automatically by loaDocumentId/invoiceDocumentId, and address-type requirements by the endUser service address. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


