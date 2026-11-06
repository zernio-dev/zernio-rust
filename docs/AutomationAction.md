# AutomationAction

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**step** | **String** | The id of the step that made it, for example `budget`. | 
**r#type** | **Type** |  (enum: ads.pause, ads.activate, ads.set_budget, ads.duplicate, ads.edit_name, ads.set_bid, ads.set_target, ads.reallocate_budget) | 
**status** | **Status** |  (enum: applied, skipped, failed) | 
**reason** | **String** | Why it was skipped or failed, such as `already_paused`, `daily_limit_reached` or `awaiting_approval`. | 
**previous** | [**models::AutomationChangedValue**](AutomationChangedValue.md) |  | 
**target** | [**models::AutomationChangedValue**](AutomationChangedValue.md) |  | 
**id** | **String** |  | 
**automation_id** | **String** |  | 
**automation_name** | **String** |  | 
**check_id** | **String** |  | 
**subject** | [**models::AutomationActionAllOfSubject**](AutomationActionAllOfSubject.md) |  | 
**platform** | **String** |  | 
**ad_account** | [**models::AutomationActionAllOfAdAccount**](AutomationActionAllOfAdAccount.md) |  | 
**currency** | Option<**String**> |  | 
**created_at** | **String** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


