# CreateLeadRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** | The profile the lead belongs to. | 
**email** | Option<**String**> | Required unless phone is given. | [optional]
**phone** | Option<**String**> | Required unless email is given. E.164 is best. | [optional]
**fields** | Option<**std::collections::HashMap<String, String>**> | Other answers, field name to value (`full_name`, `company`, ...). Stored on the lead, never sent to an ad platform. | [optional]
**form_id** | Option<**String**> | Your id for the form. Defaults to `api`. | [optional]
**form_name** | Option<**String**> |  | [optional]
**lead_id** | Option<**String**> | Your id for this lead (a CRM id, a submission id). Makes the call idempotent. | [optional]
**submitted_at** | Option<**String**> | When the form was submitted. Defaults to now. | [optional]
**source_url** | Option<**String**> | The page the form was submitted on, with its query string. | [optional]
**visitor_id** | Option<**String**> | The Zernio tag visitor id, from the `_zid` cookie. | [optional]
**click_ids** | Option<**std::collections::HashMap<String, String>**> | Ad click and browser ids: `fbclid` or `fbc`, `fbp`, `gclid`, `gbraid`, `wbraid`, `ttclid`, `msclkid`, `li_fat_id`, ... | [optional]
**utm** | Option<**std::collections::HashMap<String, String>**> | `utm_source`, `utm_campaign`, ... | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


