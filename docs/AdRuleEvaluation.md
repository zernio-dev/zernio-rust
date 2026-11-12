# AdRuleEvaluation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**evaluated_at** | **String** |  | 
**today** | [**String**](String.md) | The ad account's calendar date the windows were resolved against. | 
**timezone** | **String** | IANA timezone of the ad account. | 
**timezone_assumed** | **bool** | True when the ad account has no known timezone and UTC was assumed. | 
**currency** | Option<**String**> |  | 
**hourly_through** | Option<**String**> | Where the hourly windows (`last_complete_hour`, `last_3h`, `today_so_far`) ended: the end of the latest hour a sync has settled. Null when the rule has none or they could not be read. | [optional]
**matched** | **i32** | How many objects meet every condition. | 
**objects** | [**Vec<models::AdRuleObjectEvaluation>**](AdRuleObjectEvaluation.md) | Every delivering campaign or ad set in scope (for an `activate` rule, the rule-paused ones it may reactivate). | 
**groups** | Option<[**Vec<models::AdRuleEvaluationGroupsInner>**](AdRuleEvaluationGroupsInner.md)> | Each group's totals, for a rule with groups. Null otherwise. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


