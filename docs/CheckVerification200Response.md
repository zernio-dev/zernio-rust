# CheckVerification200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**status** | Option<**Status**> |  (enum: pending, approved, expired, max_attempts_reached, canceled, delivery_failed) | [optional]
**channel** | Option<**Channel**> |  (enum: sms, whatsapp) | [optional]
**to** | Option<**String**> |  | [optional]
**expires_at** | Option<**String**> |  | [optional]
**attempts** | Option<**i32**> |  | [optional]
**max_attempts** | Option<**i32**> |  | [optional]
**send_count** | Option<**i32**> | Accepted deliveries (initial send + resends); each bills one verification fee. | [optional]
**last_sent_at** | Option<**String**> |  | [optional]
**delivery_status** | Option<**DeliveryStatus**> | WhatsApp only, returned by GET /v1/verify/verifications/{verificationId} (null on create and check responses): what Meta reported for the latest send, null until it reports. A code that never reached the recipient (for example a number not on WhatsApp) reads failed, with the Meta error in deliveryErrorCode. failed does not settle the verification: Meta can report failed and later deliver the same message. Reported for at least an hour after the send, well past any code's expiry. (enum: delivered, read, failed, ) | [optional]
**delivery_error_code** | Option<**i32**> | Meta error code when deliveryStatus is failed (e.g. 131026, message undeliverable). | [optional]
**created_at** | Option<**String**> |  | [optional]
**resend** | Option<**bool**> | Present on create responses: true when an active verification was resent instead of created. | [optional]
**valid** | Option<**bool**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


