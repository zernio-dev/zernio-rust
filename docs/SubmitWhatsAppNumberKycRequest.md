# SubmitWhatsAppNumberKycRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** |  | 
**country** | **String** |  | 
**reuse** | Option<**bool**> | Reuse a prior approved verification for this country (skips document/field collection; places the order immediately). | [optional]
**end_user_first_name** | Option<**String**> | End user's legal first name. Required when the country has an action/ID-verification (Onfido) requirement. | [optional]
**end_user_last_name** | Option<**String**> | End user's legal last name. Same condition as endUserFirstName. | [optional]
**values** | Option<**std::collections::HashMap<String, String>**> | requirementId → textual value | [optional]
**documents** | Option<[**Vec<models::SubmitWhatsAppNumberKycRequestDocumentsInner>**](SubmitWhatsAppNumberKycRequestDocumentsInner.md)> |  | [optional]
**address** | Option<[**models::SubmitWhatsAppNumberKycRequestAddress**](SubmitWhatsAppNumberKycRequestAddress.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


