# GetLeadForm200ResponseForm

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**status** | Option<**Status**> | ARCHIVED forms can't receive new leads. (enum: ACTIVE, ARCHIVED) | [optional]
**locale** | Option<**String**> |  | [optional]
**created_time** | Option<**String**> |  | [optional]
**leads_count** | Option<**i32**> |  | [optional]
**privacy_policy_url** | Option<**String**> |  | [optional]
**follow_up_action_url** | Option<**String**> |  | [optional]
**questions** | Option<[**Vec<models::GetLeadForm200ResponseFormQuestionsInner>**](GetLeadForm200ResponseFormQuestionsInner.md)> |  | [optional]
**thank_you_page** | Option<[**models::GetLeadForm200ResponseFormThankYouPage**](GetLeadForm200ResponseFormThankYouPage.md)> |  | [optional]
**context_card** | Option<**serde_json::Value**> | Intro card shown before the form questions (title, content, button label). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


