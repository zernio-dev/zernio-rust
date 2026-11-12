# AutomationOneOf1

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** |  | 
**status** | **Status** |  (enum: active, paused) | 
**trigger** | [**models::AutomationEventTrigger**](AutomationEventTrigger.md) |  | 
**steps** | [**Vec<models::AutomationNotifyStep>**](AutomationNotifyStep.md) | May be empty: an automation with no steps only records each event it matches as a check with outcome `triggered` and no action. `limits.cooldown` and `limits.maxChangesPerDay` count actions, so they do nothing for it. | 
**limits** | Option<[**models::AutomationEventLimits**](AutomationEventLimits.md)> |  | [optional]
**id** | **String** |  | 
**kind** | **Kind** |  (enum: event) | 
**version** | **String** | Send it back as `If-Match` when editing, so an edit made after someone else saved is refused. | 
**last_check_at** | **String** | Null until an ad rule first checks. Always null for event and scheduled automations; their checks list when they ran. | 
**next_check_at** | **String** | Null while paused. Always null for event and scheduled automations. | 
**created_at** | **String** |  | 
**updated_at** | **String** |  | 
**template** | Option<[**models::AutomationRecordTemplate**](AutomationRecordTemplate.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


