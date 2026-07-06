# SubmitPhoneNumberKyc200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | Option<**Status**> |  (enum: kyc_submitted, kyc_reused, kyc_already_submitted) | [optional]
**phone_number** | Option<[**models::SubmitPhoneNumberKyc200ResponsePhoneNumber**](SubmitPhoneNumberKyc200ResponsePhoneNumber.md)> |  | [optional]
**numbers** | Option<[**Vec<models::SubmitPhoneNumberKyc200ResponseNumbersInner>**](SubmitPhoneNumberKyc200ResponseNumbersInner.md)> | Every number provisioned from this submission. Length equals the requested `quantity` on full success (fewer if some orders failed; best-effort). The first element mirrors `phoneNumber`. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


