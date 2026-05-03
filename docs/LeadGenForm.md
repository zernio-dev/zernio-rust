# LeadGenForm

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**status** | Option<**Status**> |  (enum: ACTIVE, ARCHIVED, DELETED, DRAFT) | [optional]
**locale** | Option<**String**> |  | [optional]
**created_time** | Option<**String**> |  | [optional]
**leads_count** | Option<**i32**> | Total leads (real + organic). | [optional]
**organic_leads_count** | Option<**i32**> |  | [optional]
**expired_leads_count** | Option<**i32**> |  | [optional]
**questions** | Option<[**Vec<models::LeadGenFormQuestion>**](LeadGenFormQuestion.md)> |  | [optional]
**privacy_policy_url** | Option<**String**> |  | [optional]
**follow_up_action_url** | Option<**String**> |  | [optional]
**thank_you_page** | Option<**serde_json::Value**> |  | [optional]
**context_card** | Option<**serde_json::Value**> |  | [optional]
**question_page_custom_headline** | Option<**String**> |  | [optional]
**is_optimized_for_quality** | Option<**bool**> |  | [optional]
**page_id** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


