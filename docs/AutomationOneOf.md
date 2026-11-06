# AutomationOneOf

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** |  | 
**status** | **Status** |  (enum: active, paused) | 
**trigger** | [**models::AutomationScheduleTrigger**](AutomationScheduleTrigger.md) |  | 
**subjects** | [**models::AutomationSubjects**](AutomationSubjects.md) |  | 
**conditions** | [**models::AdRuleConditions**](AdRuleConditions.md) |  | 
**alert** | Option<[**models::AutomationAlert**](AutomationAlert.md)> |  | [optional]
**steps** | [**Vec<models::AutomationStep>**](AutomationStep.md) |  | 
**limits** | Option<[**models::AutomationLimits**](AutomationLimits.md)> |  | [optional]
**id** | **String** |  | 
**kind** | **Kind** |  (enum: ad_rule) | 
**version** | **String** | Send it back as `If-Match` when editing, so an edit made after someone else saved is refused. | 
**last_check_at** | **String** | Null until an ad rule first checks. Always null for event and scheduled automations; their checks list when they ran. | 
**next_check_at** | **String** | Null while paused. Always null for event and scheduled automations. | 
**created_at** | **String** |  | 
**updated_at** | **String** |  | 
**template** | Option<[**models::AutomationRecordTemplate**](AutomationRecordTemplate.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


