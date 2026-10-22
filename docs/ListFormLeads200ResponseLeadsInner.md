# ListFormLeads200ResponseLeadsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Meta leadgenId. | [optional]
**lead_id** | Option<**String**> | Zernio lead id, for PATCH /v1/ads/leads/{id}. Only on persisted leads. | [optional]
**status** | Option<**String**> | Lead status (see PATCH /v1/ads/leads/{id}). Only on persisted leads. | [optional]
**created_time** | Option<**String**> |  | [optional]
**ad_id** | Option<**String**> |  | [optional]
**form_id** | Option<**String**> |  | [optional]
**fields** | Option<**std::collections::HashMap<String, String>**> |  | [optional]
**field_data** | Option<**Vec<serde_json::Value>**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


