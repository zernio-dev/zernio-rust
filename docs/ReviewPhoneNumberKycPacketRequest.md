# ReviewPhoneNumberKycPacketRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**country** | **String** |  | 
**number_type** | **String** |  | 
**values** | Option<**std::collections::HashMap<String, String>**> | requirementId to declared textual value. | [optional]
**address** | Option<**std::collections::HashMap<String, String>**> | Declared address (street_address, locality, ...), so a mismatched proof-of-address can be flagged. | [optional]
**docs** | [**Vec<models::SubmitPhoneNumberKycRequestDocumentsInnerOneOf1>**](SubmitPhoneNumberKycRequestDocumentsInnerOneOf1.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


