# OnBrandedCallingIdentityStatusUpdatedRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Stable webhook event ID: the dedupe key, also sent as the X-Zernio-Event-Id header and identical on every retry and redelivery. It identifies the event only, never an account or other resource. | [optional]
**event** | Option<**Event**> |  (enum: branded_calling.identity.status_updated) | [optional]
**timestamp** | Option<**String**> | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. | [optional]
**identity** | Option<[**models::OnBrandedCallingIdentityStatusUpdatedRequestIdentity**](OnBrandedCallingIdentityStatusUpdatedRequestIdentity.md)> |  | [optional]
**status** | Option<**Status**> |  (enum: requested, changes_requested, rejected, pending_email_verification, in_review, verified, suspended, expired, permanently_rejected) | [optional]
**reason** | Option<**String**> | Our review note, or the carrier's rejection reasons, when there is one. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


