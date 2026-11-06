# AutomationBacktestDayActionsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**subject** | [**models::AutomationBacktestDayActionsInnerSubject**](AutomationBacktestDayActionsInnerSubject.md) |  | 
**group** | Option<**String**> | For an automation with groups, the group the campaign was judged in. | [optional]
**r#type** | **Type** |  (enum: ads.pause, ads.activate, ads.set_budget, ads.duplicate, ads.edit_name, ads.set_bid, ads.set_target, ads.reallocate_budget, notify.send) | 
**budget** | Option<[**models::AutomationBacktestDayActionsInnerBudget**](AutomationBacktestDayActionsInnerBudget.md)> |  | [optional]
**skipped** | Option<**Skipped**> | Why it would have been skipped. Absent when it would have acted. (enum: budget_unknown, at_limit, already_at_amount) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


