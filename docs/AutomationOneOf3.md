# AutomationOneOf3

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** |  | 
**description** | Option<**String**> |  | [optional]
**status** | **Status** | Only a sequence can be a draft. (enum: draft, active, paused) | 
**trigger** | [**models::SequenceAutomationDefinitionTrigger**](SequenceAutomationDefinitionTrigger.md) |  | 
**steps** | [**Vec<models::AutomationSequenceStep>**](AutomationSequenceStep.md) | At least one step for an active sequence. Steps change only while it is a draft or paused. | 
**limits** | Option<[**models::SequenceAutomationDefinitionLimits**](SequenceAutomationDefinitionLimits.md)> |  | [optional]
**id** | **String** |  | 
**kind** | **Kind** |  (enum: sequence) | 
**version** | **String** | Send it back as `If-Match` when editing, so an edit made after someone else saved is refused. | 
**last_check_at** | **String** | Null until an ad rule first checks. Always null for event and scheduled automations; their checks list when they ran. | 
**next_check_at** | **String** | Null while paused. Always null for event, scheduled and sequence automations. | 
**created_at** | **String** |  | 
**updated_at** | **String** |  | 
**template** | Option<[**models::AutomationRecordTemplate**](AutomationRecordTemplate.md)> |  | [optional]
**platform** | **String** | The account's platform. On `whatsapp` every step sends a template. | 
**enrollments** | [**models::AutomationOneOf3AllOfEnrollments**](AutomationOneOf3AllOfEnrollments.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


