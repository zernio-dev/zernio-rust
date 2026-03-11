# CreateWhatsAppContactRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account ID | 
**phone** | **String** | Phone number in E.164 format | 
**name** | **String** | Contact name | 
**email** | Option<**String**> | Contact email | [optional]
**company** | Option<**String**> | Company name | [optional]
**tags** | Option<**Vec<String>**> | Tags for categorization | [optional]
**groups** | Option<**Vec<String>**> | Groups the contact belongs to | [optional]
**is_opted_in** | Option<**bool**> | Whether the contact has opted in to receive messages | [optional][default to true]
**custom_fields** | Option<**std::collections::HashMap<String, String>**> | Custom key-value fields | [optional]
**notes** | Option<**String**> | Notes about the contact | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


