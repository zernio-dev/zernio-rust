# AutomationRecord

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**kind** | **Kind** |  (enum: ad_rule, event, scheduled, sequence, comment, workflow) | 
**status** | **Status** | Only a sequence or a flow can be a draft. (enum: draft, active, paused) | 
**version** | **String** | Send it back as `If-Match` when editing, so an edit made after someone else saved is refused. | 
**last_check_at** | Option<**String**> | Null until an ad rule first checks. Always null for every other kind; the checks of event and scheduled automations list when they ran. | 
**next_check_at** | Option<**String**> | Null while paused. Always null for every kind but ad rules. | 
**created_at** | **String** |  | 
**updated_at** | **String** |  | 
**template** | Option<[**models::AutomationRecordTemplate**](AutomationRecordTemplate.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


