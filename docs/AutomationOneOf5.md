# AutomationOneOf5

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** |  | 
**description** | Option<**String**> |  | [optional]
**status** | **Status** | Only a sequence or a flow can be a draft. (enum: draft, active, paused) | 
**trigger** | [**models::FlowAutomationDefinitionTrigger**](FlowAutomationDefinitionTrigger.md) |  | 
**graph** | [**models::FlowAutomationDefinitionGraph**](FlowAutomationDefinitionGraph.md) |  | 
**id** | **String** |  | 
**kind** | **Kind** |  (enum: workflow) | 
**version** | **String** | Send it back as `If-Match` when editing, so an edit made after someone else saved is refused. | 
**last_check_at** | **String** | Null until an ad rule first checks. Always null for every other kind; the checks of event and scheduled automations list when they ran. | 
**next_check_at** | **String** | Null while paused. Always null for every kind but ad rules. | 
**created_at** | **String** |  | 
**updated_at** | **String** |  | 
**template** | Option<[**models::AutomationRecordTemplate**](AutomationRecordTemplate.md)> |  | [optional]
**platform** | **String** | The account's platform. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


