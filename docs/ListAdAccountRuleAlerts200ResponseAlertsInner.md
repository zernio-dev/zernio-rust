# ListAdAccountRuleAlerts200ResponseAlertsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**rule_id** | **String** | The rule the alert belongs to. | 
**id** | **String** |  | 
**object_id** | **String** | Platform campaign, ad set or ad ID, or the id of the keyword or search term. | 
**state** | **State** |  (enum: open) | 
**severity** | Option<**Severity**> |  (enum: warning, critical, ) | 
**consecutive_matches** | **i32** |  | 
**opened_at** | Option<**String**> |  | 
**last_matched_at** | **String** |  | 
**last_evaluated_at** | **String** | When a run last evaluated the object of this alert. Older than the latest run of its rule means that run did not evaluate it. | 
**resolved_at** | Option<**String**> | Always null here: only open alerts are listed. | 
**resolved_reason** | Option<**String**> | Always null here: only open alerts are listed. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


