# ListLocalServicesLeads200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Lead id; pass to /v1/ads/local-services/leads/{leadId}/conversations. | [optional]
**lead_type** | Option<**String**> | PHONE_CALL / MESSAGE / BOOKING. | [optional]
**category_id** | Option<**String**> |  | [optional]
**service_id** | Option<**String**> |  | [optional]
**contact** | Option<[**models::ListLocalServicesLeads200ResponseDataInnerContact**](ListLocalServicesLeads200ResponseDataInnerContact.md)> |  | [optional]
**status** | Option<**String**> |  | [optional]
**created_time** | Option<**String**> | Google datetime in the customer's timezone (YYYY-MM-DD HH:MM:SS). | [optional]
**locale** | Option<**String**> |  | [optional]
**charged** | Option<**bool**> |  | [optional]
**credit_state** | Option<**String**> |  | [optional]
**credit_state_last_update** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


