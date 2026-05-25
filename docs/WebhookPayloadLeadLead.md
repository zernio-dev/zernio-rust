# WebhookPayloadLeadLead

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Zernio lead ID (AdLead document ID) | 
**leadgen_id** | **String** | Meta lead ID (the platform's leadgen_id) | 
**form_id** | **String** | Lead Gen form ID the lead was submitted against | 
**form_name** | Option<**String**> | Human-readable form name (best-effort; may be null) | [optional]
**ad_id** | Option<**String**> | Meta ad ID that drove the lead (null for organic/test leads) | [optional]
**adset_id** | Option<**String**> |  | [optional]
**campaign_id** | Option<**String**> |  | [optional]
**fields** | **std::collections::HashMap<String, String>** | Flattened question key -> answer map. For multiple-choice questions the value is the option key (e.g. \"k1\"), not the display label.  | 
**is_organic** | **bool** | True when the lead came from an organic post rather than a paid ad | 
**created_at** | **String** | Meta's lead creation time (ISO 8601) | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


