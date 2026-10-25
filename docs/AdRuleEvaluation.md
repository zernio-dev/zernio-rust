# AdRuleEvaluation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**evaluated_at** | **String** |  | 
**today** | [**String**](String.md) | The ad account's calendar date the windows were resolved against. | 
**timezone** | **String** | IANA timezone of the ad account. | 
**timezone_assumed** | **bool** | True when the ad account has no known timezone and UTC was assumed. | 
**currency** | Option<**String**> |  | 
**matched** | **i32** | How many objects meet every condition. | 
**objects** | [**Vec<models::AdRuleObjectEvaluation>**](AdRuleObjectEvaluation.md) | Every delivering campaign or ad set in scope (for an `activate` rule, the rule-paused ones it may reactivate). | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


