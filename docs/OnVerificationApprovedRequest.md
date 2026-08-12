# OnVerificationApprovedRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**event** | Option<**Event**> |  (enum: verification.approved) | [optional]
**timestamp** | Option<**String**> | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. | [optional]
**verification** | Option<[**models::OnVerificationApprovedRequestVerification**](OnVerificationApprovedRequestVerification.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


