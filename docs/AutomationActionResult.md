# AutomationActionResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**step** | **String** | The id of the step that made it, for example `budget`. | 
**r#type** | **Type** |  (enum: ads.pause, ads.activate, ads.set_budget, ads.duplicate, ads.edit_name, ads.set_bid, ads.set_target, ads.reallocate_budget) | 
**status** | **Status** |  (enum: applied, skipped, failed) | 
**reason** | Option<**String**> | Why it was skipped or failed, such as `already_paused`, `daily_limit_reached` or `awaiting_approval`. | 
**previous** | [**models::AutomationChangedValue**](AutomationChangedValue.md) |  | 
**target** | [**models::AutomationChangedValue**](AutomationChangedValue.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


