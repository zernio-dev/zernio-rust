# MetaLeadFormQuestionsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**key** | Option<**String**> |  | [optional]
**label** | Option<**String**> |  | [optional]
**r#type** | Option<**String**> | EMAIL, PHONE, FULL_NAME, CUSTOM, ... | [optional]
**inline_context** | Option<**String**> |  | [optional]
**options** | Option<[**Vec<models::BoostPostRequestTrackingUrlTagsInner>**](BoostPostRequestTrackingUrlTagsInner.md)> |  | [optional]
**conditional_questions_group_id** | Option<**String**> | READ-ONLY. Conditional logic can only be authored in Meta form builder; Meta has no create parameter for it. | [optional]
**conditional_questions_choices** | Option<**Vec<serde_json::Value>**> | READ-ONLY. Which answers reveal the conditional group. | [optional]
**dependent_conditional_questions** | Option<**Vec<serde_json::Value>**> | READ-ONLY. Questions revealed by the conditional group. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


