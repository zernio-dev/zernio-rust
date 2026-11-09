# WebhookPayloadLeadLead

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Zernio lead ID (AdLead document ID) | 
**platform** | Option<**Platform**> | The ad network the lead came from. (enum: meta, google, linkedin, tiktok, ) | [optional]
**leadgen_id** | **String** | The network's lead id: Meta's leadgen_id, or the Google lead form submission id | 
**form_id** | **String** | Lead Gen form ID the lead was submitted against | 
**form_name** | Option<**String**> | Human-readable form name (best-effort; may be null) | [optional]
**ad_id** | Option<**String**> | Meta ad ID that drove the lead (null for organic/test leads) | [optional]
**adset_id** | Option<**String**> |  | [optional]
**campaign_id** | Option<**String**> |  | [optional]
**fields** | **std::collections::HashMap<String, String>** | Flattened question key -> answer map. For multiple-choice questions the value is the option key (e.g. \"k1\"), not the display label.  | 
**consents** | Option<[**Vec<models::AdLeadConsent>**](AdLeadConsent.md)> | Sent on every delivery since 2026-10-25. Absent when an older event is redelivered, since redeliveries replay the stored payload. | [optional]
**is_organic** | **bool** | True when the lead came from an organic post rather than a paid ad | 
**created_at** | **String** | Meta's lead creation time (ISO 8601) | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


