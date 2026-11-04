# ListAdRuleAlerts200ResponseAlertsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**object_id** | **String** | Platform campaign, ad set or ad ID. | 
**state** | **State** |  (enum: pending, open, resolved) | 
**severity** | Option<**Severity**> |  (enum: warning, critical, ) | 
**consecutive_matches** | **i32** |  | 
**opened_at** | Option<**String**> |  | 
**last_matched_at** | **String** |  | 
**resolved_at** | Option<**String**> |  | 
**resolved_reason** | Option<**ResolvedReason**> |  (enum: condition_cleared, action_applied, not_evaluated, automation_changed, automation_off, ) | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


