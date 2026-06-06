# GetWhatsAppPhoneNumbers200ResponseNumbersInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | Option<**String**> |  | [optional]
**phone_number** | Option<**String**> |  | [optional]
**country** | Option<**String**> |  | [optional]
**status** | Option<**Status**> |  (enum: pending_payment, pending_regulatory, regulatory_declined, provisioning, verifying, active, suspended, releasing, released) | [optional]
**registrant_name** | Option<**String**> | For regulated numbers | [optional]
**telnyx_order_id** | Option<**String**> | Present once the number order has been placed (i.e. the requirement group was approved). Absent while still in identity review. | [optional]
**monthly_cents** | Option<**i32**> | Per-country monthly price in cents ($2..$25). | [optional]
**profile_id** | Option<**serde_json::Value**> |  | [optional]
**provisioned_at** | Option<**String**> |  | [optional]
**meta_preverified_id** | Option<**String**> |  | [optional]
**meta_verification_status** | Option<**String**> |  | [optional]
**onfido_verification_url** | Option<**String**> | For regulated (Tier 3/4) numbers with an Onfido ID-verification step — the link to forward to the end user. Set once the order is placed; null otherwise. Poll this field after submitting KYC. | [optional]
**end_user_first_name** | Option<**String**> |  | [optional]
**end_user_last_name** | Option<**String**> |  | [optional]
**regulatory_decline_reason** | Option<**String**> | Reviewer rejection reason when status is regulatory_declined. | [optional]
**created_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


