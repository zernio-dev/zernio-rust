# AutomationApproval

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**automation_id** | **String** |  | 
**check_id** | **String** | The check that found the matches and sent the request. | 
**status** | **Status** | `cancelled` when the automation stopped asking for approval before anyone decided. (enum: pending, approved, rejected, expired, cancelled) | 
**to** | **Vec<String>** | The emails the request was sent to. | 
**expires_at** | **String** | After this the request can no longer be decided and its changes are skipped. | 
**created_at** | **String** |  | 
**decided_by** | [**models::AutomationApprovalDecidedBy**](AutomationApprovalDecidedBy.md) |  | 
**decided_at** | Option<**String**> |  | 
**can_decide** | **bool** | True when the request is pending and you are one of the approvers the automation names now. | 
**changes** | [**Vec<models::AutomationApprovalChange>**](AutomationApprovalChange.md) | The changes the request holds. Notifications are not listed. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


