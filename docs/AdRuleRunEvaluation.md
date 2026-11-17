# AdRuleRunEvaluation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**unread_objects** | Option<**i32**> | On a run that matched nothing: how many objects had a condition whose value could not be read, so they could not match. A campaign with under 3 of the 4 previous weeks of data has no `usual` yet. | [optional]
**rule** | Option<[**models::AdRuleRunEvaluationRule**](AdRuleRunEvaluationRule.md)> |  | [optional]
**today** | Option<[**String**](String.md)> |  | [optional]
**timezone** | Option<**String**> |  | [optional]
**timezone_assumed** | Option<**bool**> |  | [optional]
**currency** | Option<**String**> |  | [optional]
**hourly_through** | Option<**String**> | Where the run's hourly windows ended. Absent on runs recorded before November 2026. | [optional]
**matched** | Option<[**Vec<models::AdRuleObjectEvaluation>**](AdRuleObjectEvaluation.md)> | The matched objects, at most 200. `matchedTotal` has the full count. | [optional]
**matched_total** | Option<**i32**> | How many objects matched, including those past the 200 recorded. Absent on runs recorded before November 2026. | [optional]
**actions** | Option<[**Vec<models::AdRuleRunEvaluationActionsInner>**](AdRuleRunEvaluationActionsInner.md)> |  | [optional]
**notification** | Option<[**models::AdRuleRunEvaluationNotification**](AdRuleRunEvaluationNotification.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


