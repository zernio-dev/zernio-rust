# AdLead

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
**consents** | Option<[**Vec<models::AdLeadConsent>**](AdLeadConsent.md)> | Meta lead forms only: the answer to every custom disclaimer checkbox, required or optional. Empty when the form has none, and may be empty on leads stored before 2026-10-22. LinkedIn leads do not carry the field. | [optional]
**status** | Option<**Status**> | Meta leads only. `contacted` is set when the first WhatsApp message of a lead_received workflow is delivered, `unreachable` when it fails or the phone number is not valid. (enum: new, contacted, unreachable, qualified, converted, disqualified) | [optional]
**status_changed_at** | Option<**String**> |  | [optional]
**value** | Option<**f64**> |  | [optional]
**currency** | Option<**String**> |  | [optional]
**contact_id** | Option<**String**> | The contact a lead_received workflow created or matched for this lead. | [optional]
**first_contacted_at** | Option<**String**> | When the first WhatsApp message to the lead was delivered. | [optional]
**conversation_id** | Option<**String**> | The Inbox conversation a lead_received workflow opened with the lead. | [optional]
**webhook_delivered_at** | Option<**String**> | Meta leads only. When the `lead.received` webhook was delivered; null while it has not been. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


