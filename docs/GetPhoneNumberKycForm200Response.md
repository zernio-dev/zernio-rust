# GetPhoneNumberKycForm200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**country** | Option<**String**> |  | [optional]
**number_type** | Option<**String**> |  | [optional]
**fields** | Option<[**Vec<models::GetPhoneNumberKycForm200ResponseFieldsInner>**](GetPhoneNumberKycForm200ResponseFieldsInner.md)> |  | [optional]
**reusable** | Option<[**models::GetPhoneNumberKycForm200ResponseReusable**](GetPhoneNumberKycForm200ResponseReusable.md)> |  | [optional]
**pending_review** | Option<**bool**> | true when this account already has a number for this country in regulatory review (status pending_regulatory). Scope is the whole account across all profiles, and the country only (any number type), so it is not a per-end-client signal on a multi-tenant setup. Informational only: it never blocks a submission, and several same-country numbers may sit in review at once. For a per-end-client view, call GET /v1/phone-numbers with `profileId` and `status=pending_regulatory`; that view also lists numbers declined in the last 30 days. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


