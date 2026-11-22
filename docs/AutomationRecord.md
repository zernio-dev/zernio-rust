# AutomationRecord

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**kind** | **Kind** |  (enum: ad_rule, event, scheduled, sequence, comment) | 
**status** | **Status** | Only a sequence can be a draft. (enum: draft, active, paused) | 
**version** | **String** | Send it back as `If-Match` when editing, so an edit made after someone else saved is refused. | 
**last_check_at** | Option<**String**> | Null until an ad rule first checks. Always null for event and scheduled automations; their checks list when they ran. | 
**next_check_at** | Option<**String**> | Null while paused. Always null for event, scheduled and sequence automations. | 
**created_at** | **String** |  | 
**updated_at** | **String** |  | 
**template** | Option<[**models::AutomationRecordTemplate**](AutomationRecordTemplate.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


