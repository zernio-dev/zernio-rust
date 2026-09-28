# BrandedCallingIdentityNumber

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**phone_number_id** | Option<**String**> |  | [optional]
**phone_number** | Option<**String**> |  | [optional]
**status** | Option<**Status**> | verified = the identity shows on calls from this number. permanently_rejected cannot be attached again anywhere. (enum: submitted, in_review, verified, unsuccessful, suspended, expired, permanently_rejected) | [optional]
**rejection_reason** | Option<[**models::BrandedCallingIdentityNumberRejectionReason**](BrandedCallingIdentityNumberRejectionReason.md)> |  | [optional]
**verified_at** | Option<**String**> |  | [optional]
**added_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


