# AudienceUploadUser

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | Option<**String**> | Email, or SHA-256 of it trimmed and lowercased. | [optional]
**phone** | Option<**String**> | Phone with country code. Plaintext matches on Meta and Google; see the endpoint description before sending it hashed. | [optional]
**first_name** | Option<**String**> |  | [optional]
**last_name** | Option<**String**> |  | [optional]
**birth_year** | Option<**String**> | YYYY. Meta only. | [optional]
**birth_month** | Option<**String**> | MM (01-12). Meta only. | [optional]
**birth_day** | Option<**String**> | DD (01-31). Meta only. | [optional]
**gender** | Option<**String**> | m or f. Meta only. | [optional]
**city** | Option<**String**> | Meta only. | [optional]
**state** | Option<**String**> | Meta only. | [optional]
**zip** | Option<**String**> |  | [optional]
**country** | Option<**String**> | ISO 3166-1 alpha-2 code. | [optional]
**external_id** | Option<**String**> | Your own id for the person. Meta only. | [optional]
**region** | Option<**String**> | Where the person is (ISO country, or US-CA). With no granted consent, EEA, UK and CH people are dropped before upload. | [optional]
**consent** | Option<[**models::AudienceUploadUserConsent**](AudienceUploadUserConsent.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


