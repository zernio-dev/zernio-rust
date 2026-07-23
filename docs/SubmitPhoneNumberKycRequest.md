# SubmitPhoneNumberKycRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** |  | 
**country** | **String** |  | 
**submission_id** | Option<**String**> | Idempotency token for this submission attempt. A retry/double-submit with the same token returns the same number; omit and each call creates a new number. | [optional]
**quantity** | Option<**i32**> | Provision several same-country numbers from one submission (1-5). The single verification covers all of them; each number is billed only when it activates. Numbers that fail to order are skipped (best-effort). | [optional][default to 1]
**reuse** | Option<**bool**> | Reuse a prior approved verification for this country (skips document/field collection; places the order immediately). | [optional]
**reuse_option_id** | Option<**String**> | Which reusable verification to use (GET reusable.options[].id). The unambiguous selection key. Omitted = the approved default. No match = 409. | [optional]
**reuse_from** | Option<**String**> | Legacy fallback for `reuseOptionId`: the source phone number (GET reusable.options[].fromPhoneNumber). Ambiguous when a number labels two verifications — prefer `reuseOptionId`. Omitted = the approved default. No match = 409. | [optional]
**end_user_first_name** | Option<**String**> | End user's legal first name. Required when the country has an action/ID-verification (Onfido) requirement. | [optional]
**end_user_last_name** | Option<**String**> | End user's legal last name. Same condition as endUserFirstName. | [optional]
**values** | Option<**std::collections::HashMap<String, String>**> | requirementId → textual value | [optional]
**documents** | Option<[**Vec<models::SubmitPhoneNumberKycRequestDocumentsInner>**](SubmitPhoneNumberKycRequestDocumentsInner.md)> | One per document requirement. Each is EITHER inline base64 OR a `documentId` returned by POST /v1/phone-numbers/kyc/upload-document (use the upload endpoint for large files to stay under the request-size limit). | [optional]
**address** | Option<[**models::SubmitPhoneNumberKycRequestAddress**](SubmitPhoneNumberKycRequestAddress.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


