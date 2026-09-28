# BrandedCallingIdentity

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**enterprise_id** | Option<**String**> |  | [optional]
**display_name** | Option<**String**> |  | [optional]
**call_reasons** | Option<**Vec<String>**> |  | [optional]
**call_reasons_pre_approved** | Option<**bool**> | Every call reason matches the carrier catalogue (GET /v1/branded-calling/call-reasons); anything else is vetted by hand and takes longer. | [optional]
**logo_url** | Option<**String**> | The image you sent. Zernio hosts the 256x256 BMP the carriers require. | [optional]
**authorizer** | Option<[**models::BrandedCallingIdentityAuthorizer**](BrandedCallingIdentityAuthorizer.md)> |  | [optional]
**references** | Option<[**models::BrandedCallingReferences**](BrandedCallingReferences.md)> |  | [optional]
**status** | Option<**Status**> | requested = in Zernio review; changes_requested = answer the review (PATCH); pending_email_verification = confirm the code emailed to the authorizer; in_review = with the carrier vetting team; verified = attach numbers; rejected = fix and PATCH to resubmit; suspended = an infringement claim is open; expired = the yearly verification lapsed; permanently_rejected = terminal. (enum: requested, changes_requested, rejected, pending_email_verification, in_review, verified, suspended, expired, permanently_rejected) | [optional]
**rejection_reasons** | Option<[**Vec<models::BrandedCallingIdentityRejectionReasonsInner>**](BrandedCallingIdentityRejectionReasonsInner.md)> |  | [optional]
**review_note** | Option<**String**> | The open change request, as text. | [optional]
**review_request** | Option<[**models::BrandedCallingIdentityReviewRequest**](BrandedCallingIdentityReviewRequest.md)> |  | [optional]
**email_verified_at** | Option<**String**> |  | [optional]
**submitted_at** | Option<**String**> |  | [optional]
**verified_at** | Option<**String**> |  | [optional]
**expiring_at** | Option<**String**> | Verification lasts one year; Zernio resubmits 30 days before this date. | [optional]
**numbers** | Option<[**Vec<models::BrandedCallingIdentityNumber>**](BrandedCallingIdentityNumber.md)> |  | [optional]
**created_at** | Option<**String**> |  | [optional]
**updated_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


