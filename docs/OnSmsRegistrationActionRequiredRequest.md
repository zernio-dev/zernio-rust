# OnSmsRegistrationActionRequiredRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**test** | Option<**bool**> | Always true when present: only a sample sent by POST /v1/webhooks/test with an event carries it. Real deliveries never do. | [optional]
**id** | Option<**String**> | Stable webhook event ID: the dedupe key, also sent as the X-Zernio-Event-Id header and identical on every retry and redelivery. It identifies the event only, never an account or other resource. | [optional]
**event** | Option<**Event**> |  (enum: sms.registration.action_required) | [optional]
**timestamp** | Option<**String**> | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. | [optional]
**registration** | Option<[**models::OnSmsRegistrationActionRequiredRequestRegistration**](OnSmsRegistrationActionRequiredRequestRegistration.md)> |  | [optional]
**reason** | Option<**Reason**> |  (enum: changes_requested, otp_required, carrier_info_required) | [optional]
**message** | Option<**String**> | What to do, in words: our request or the carrier's note. Absent for otp_required. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


