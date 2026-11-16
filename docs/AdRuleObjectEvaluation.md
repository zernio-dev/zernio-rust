# AdRuleObjectEvaluation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Platform ID of the campaign or ad set. | 
**name** | **String** |  | 
**campaign_id** | Option<**String**> |  | 
**matched** | **bool** | True when every condition holds. | 
**group** | Option<**String**> | For a rule with groups: the group this campaign was judged in. `matched` and `conditions` are the group's. | [optional]
**conditions** | [**Vec<models::AdRuleObjectEvaluationConditionsInner>**](AdRuleObjectEvaluationConditionsInner.md) |  | 
**readings** | Option<[**Vec<models::AdRuleObjectEvaluationReadingsInner>**](AdRuleObjectEvaluationReadingsInner.md)> | On a matched object: spend, impressions and clicks over each window its conditions read, and the other search impression shares when a condition reads one. Left out where a condition already reads the value. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


