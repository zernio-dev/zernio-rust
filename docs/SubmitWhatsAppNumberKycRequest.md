# SubmitWhatsAppNumberKycRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** |  | 
**country** | **String** |  | 
**submission_id** | Option<**String**> | Idempotency token for this submission attempt. Once the number has been ordered, a retry with the same token returns that same number instead of ordering another. A submission that fails before the number is ordered releases the token, so you can correct your details and re-submit with it. Omit it and every call provisions a new number. | [optional]
**quantity** | Option<**i32**> | Provision several same-country numbers from one submission (1-5). The single verification covers all of them; each number is billed only when it activates. Numbers that fail to order are skipped (best-effort). With `areaCode`, a quantity above that area's live stock is rejected with a 400. | [optional][default to 1]
**reuse** | Option<**bool**> | Reuse a prior approved verification for this country (skips document/field collection; places the order immediately). | [optional]
**reuse_option_id** | Option<**String**> | Which reusable verification to use (GET reusable.options[].id). The unambiguous selection key. Omitted = the approved default. No match = 409. | [optional]
**reuse_from** | Option<**String**> | Legacy fallback for `reuseOptionId`: the source phone number (GET reusable.options[].fromPhoneNumber). Ambiguous when a number labels two verifications — prefer `reuseOptionId`. Omitted = the approved default. No match = 409. | [optional]
**area_code** | Option<**String**> | Area code (NDC) the number must be in. Hard constraint: an empty area pool fails with 409 code AREA_CODE_UNAVAILABLE instead of ordering from another area. Omit for any area. Options come from GET /v1/phone-numbers/availability (areaOptions); the purchase 202 kycUrl echoes the areaCode picked at purchase time so it can be passed here. | [optional]
**end_user_first_name** | Option<**String**> | End user's legal first name. Required when the country has an action/ID-verification (Onfido) requirement. | [optional]
**end_user_last_name** | Option<**String**> | End user's legal last name. Same condition as endUserFirstName. | [optional]
**values** | Option<**std::collections::HashMap<String, String>**> | requirementId → textual value | [optional]
**documents** | Option<[**Vec<models::SubmitWhatsAppNumberKycRequestDocumentsInner>**](SubmitWhatsAppNumberKycRequestDocumentsInner.md)> | One per document requirement. Each is EITHER inline base64 OR a `documentId` returned by POST /v1/whatsapp/phone-numbers/kyc/upload-document (use the upload endpoint for large files to stay under the request-size limit). | [optional]
**address** | Option<[**models::SubmitPhoneNumberKycRequestAddress**](SubmitPhoneNumberKycRequestAddress.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


