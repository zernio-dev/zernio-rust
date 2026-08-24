# UpdateWhatsAppFlowRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account ID | 
**name** | Option<**String**> | New flow name | [optional]
**categories** | Option<**Vec<Categories>**> |  (enum: SIGN_UP, SIGN_IN, APPOINTMENT_BOOKING, LEAD_GENERATION, CONTACT_US, CUSTOMER_SUPPORT, SURVEY, OTHER) | [optional]
**endpoint_uri** | Option<**String**> | HTTPS-only data exchange endpoint for the flow. Settable only while the flow is in DRAFT, and the flow's uploaded Flow JSON must declare data_api_version \"3.0\" for the endpoint to be used. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


