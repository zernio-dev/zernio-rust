# ListLeads200ResponseLeadsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Zernio lead id. | [optional]
**leadgen_id** | Option<**String**> | Meta lead id. On LinkedIn, the leadFormResponse id. | [optional]
**form_id** | Option<**String**> |  | [optional]
**form_name** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**ad_id** | Option<**String**> |  | [optional]
**adset_id** | Option<**String**> |  | [optional]
**campaign_id** | Option<**String**> | On LinkedIn, this is the LinkedIn Campaign id, which corresponds to platformAdSetId on GET /v1/ads (LinkedIn's Campaign Group is Zernio's campaign). | [optional]
**is_organic** | Option<**bool**> |  | [optional]
**created_time** | Option<**String**> | ISO 8601. | [optional]
**fields** | Option<**std::collections::HashMap<String, String>**> | Question key → answer. On LinkedIn, the key is the lowercased predefinedField, else the question name, else the numeric questionId; multiple-choice values are option labels (unlike Meta, which returns the option key). | [optional]
**field_data** | Option<**Vec<serde_json::Value>**> | Raw Meta field_data. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


