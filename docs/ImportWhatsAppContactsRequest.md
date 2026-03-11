# ImportWhatsAppContactsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account ID | 
**contacts** | [**Vec<models::ImportWhatsAppContactsRequestContactsInner>**](ImportWhatsAppContactsRequestContactsInner.md) | Contacts to import (max 1000) | 
**default_tags** | Option<**Vec<String>**> | Tags applied to all imported contacts | [optional]
**default_groups** | Option<**Vec<String>**> | Groups applied to all imported contacts | [optional]
**skip_duplicates** | Option<**bool**> | Skip contacts with existing phone numbers | [optional][default to true]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


