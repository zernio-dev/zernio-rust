# Lead

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Meta `leadgen_id`. | [optional]
**created_time** | Option<**String**> |  | [optional]
**ad_id** | Option<**String**> | Meta ad ID that surfaced the form. Organic leads omit this. | [optional]
**form_id** | Option<**String**> |  | [optional]
**fields** | Option<**std::collections::HashMap<String, String>**> | Flattened key→value map of answers (multi-value fields joined with \", \"). | [optional]
**field_data** | Option<[**Vec<models::LeadFieldDataInner>**](LeadFieldDataInner.md)> | Raw `field_data` from Meta (one entry per question). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


