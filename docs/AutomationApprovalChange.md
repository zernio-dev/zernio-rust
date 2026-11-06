# AutomationApprovalChange

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**action_id** | **String** |  | 
**subject** | [**models::AutomationApprovalChangeSubject**](AutomationApprovalChangeSubject.md) |  | 
**r#type** | **Type** |  (enum: ads.pause, ads.activate, ads.set_budget, ads.duplicate, ads.edit_name, ads.set_bid, ads.set_target, ads.reallocate_budget) | 
**previous** | [**models::AutomationApprovalChangePrevious**](AutomationApprovalChangePrevious.md) |  | 
**target** | [**models::AutomationApprovalChangeTarget**](AutomationApprovalChangeTarget.md) |  | 
**conditions** | **Vec<serde_json::Value>** | Each condition as it was judged when the request was sent, with its actual value. | 
**status** | **Status** | `pending` until the request is decided. (enum: pending, applied, skipped, failed, unknown) | 
**reason** | Option<**String**> | Why the change was made, skipped or failed, when known. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


