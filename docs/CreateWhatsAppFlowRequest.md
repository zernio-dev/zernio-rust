# CreateWhatsAppFlowRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account ID | 
**name** | **String** | Flow display name | 
**categories** | **Vec<Categories>** | Flow categories (enum: SIGN_UP, SIGN_IN, APPOINTMENT_BOOKING, LEAD_GENERATION, CONTACT_US, CUSTOMER_SUPPORT, SURVEY, OTHER) | 
**clone_flow_id** | Option<**String**> | Optional: ID of an existing flow to clone the Flow JSON from | [optional]
**as_version** | Option<**bool**> | When cloning, true keeps the clone in cloneFlowId's version lineage (auto-numbered next version); false/absent creates an independent flow. Ignored without cloneFlowId. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


