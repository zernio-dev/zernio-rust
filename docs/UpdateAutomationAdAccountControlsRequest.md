# UpdateAutomationAdAccountControlsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | The ads connection that reaches the ad account. | 
**ad_account_id** | **String** | The platform's ad account id. | 
**paused** | Option<**bool**> | True stops every automation on this ad account; false lets them run again. | [optional]
**daily_raise_limit** | Option<**f64**> | The most automations may raise budgets on this ad account in any 24 hours, in the ad account's currency. A raise past it is cut to the room left.  Send null to remove the limit.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


