# WorkspaceWithBilling

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**personal** | Option<**bool**> | True for the caller's own Personal workspace, which is never shared, renamed or deleted. | [optional]
**role** | Option<**Role**> | The caller's role in this workspace. (enum: owner, admin, billing_admin, member, viewer) | [optional]
**created_at** | Option<**String**> |  | [optional]
**deletion_scheduled_at** | Option<**String**> | When a scheduled deletion runs; null when none is scheduled. | [optional]
**billing** | Option<[**models::WorkspaceWithBillingAllOfBilling**](WorkspaceWithBillingAllOfBilling.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


