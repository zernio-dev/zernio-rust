# Verification

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**status** | Option<**Status**> |  (enum: pending, approved, expired, max_attempts_reached, canceled, delivery_failed) | [optional]
**channel** | Option<**Channel**> |  (enum: sms) | [optional]
**to** | Option<**String**> |  | [optional]
**expires_at** | Option<**String**> |  | [optional]
**attempts** | Option<**i32**> |  | [optional]
**max_attempts** | Option<**i32**> |  | [optional]
**send_count** | Option<**i32**> | Accepted deliveries (initial send + resends); each bills one verification fee. | [optional]
**last_sent_at** | Option<**String**> |  | [optional]
**created_at** | Option<**String**> |  | [optional]
**resend** | Option<**bool**> | Present on create responses: true when an active verification was resent instead of created. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


