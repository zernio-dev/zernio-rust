# OnSmsRegistrationStatusUpdatedRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**event** | Option<**Event**> |  (enum: sms.registration.status_updated) | [optional]
**timestamp** | Option<**String**> | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. | [optional]
**registration** | Option<[**models::OnSmsRegistrationStatusUpdatedRequestRegistration**](OnSmsRegistrationStatusUpdatedRequestRegistration.md)> |  | [optional]
**status** | Option<**Status**> |  (enum: changes_requested, requested, pending, approved, rejected, deactivated) | [optional]
**reason** | Option<**String**> | The carriers' decline reason, on rejected. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


