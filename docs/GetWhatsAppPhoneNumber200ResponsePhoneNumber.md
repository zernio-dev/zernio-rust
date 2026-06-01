# GetWhatsAppPhoneNumber200ResponsePhoneNumber

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**phone_number** | Option<**String**> |  | [optional]
**status** | Option<**Status**> |  (enum: pending_payment, pending_regulatory, regulatory_declined, provisioning, active, suspended, releasing, released) | [optional]
**country** | Option<**String**> |  | [optional]
**meta_preverified_id** | Option<**String**> |  | [optional]
**meta_verification_status** | Option<**String**> |  | [optional]
**onfido_verification_url** | Option<**String**> | For a regulated number with an Onfido ID step — the link to forward to the end user. Appears once the order is placed; null otherwise. | [optional]
**end_user_first_name** | Option<**String**> |  | [optional]
**end_user_last_name** | Option<**String**> |  | [optional]
**regulatory_decline_reason** | Option<**String**> | Reviewer rejection reason when status is regulatory_declined. | [optional]
**provisioned_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


