# SubmitPhoneNumberKyc200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | Option<**Status**> |  (enum: kyc_submitted, kyc_reused, kyc_already_submitted) | [optional]
**pre_order** | Option<**bool**> | True when nothing was in stock and this submission placed a pre-order. The number stays `pending_regulatory` until the carrier sources it (usually about 3 weeks) and is not billed until active. A pre-order is one number: `quantity` above 1 is rejected with 400. | [optional]
**phone_number** | Option<[**models::SubmitPhoneNumberKyc200ResponsePhoneNumber**](SubmitPhoneNumberKyc200ResponsePhoneNumber.md)> |  | [optional]
**numbers** | Option<[**Vec<models::SubmitPhoneNumberKyc200ResponseNumbersInner>**](SubmitPhoneNumberKyc200ResponseNumbersInner.md)> | Every number provisioned from this submission. Length equals the requested `quantity` on full success (fewer if some orders failed; best-effort). The first element mirrors `phoneNumber`. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


