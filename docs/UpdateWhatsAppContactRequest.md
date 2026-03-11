# UpdateWhatsAppContactRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | Option<**String**> | Contact name | [optional]
**email** | Option<**String**> | Contact email | [optional]
**company** | Option<**String**> | Company name | [optional]
**tags** | Option<**Vec<String>**> | Tags (replaces existing) | [optional]
**groups** | Option<**Vec<String>**> | Groups (replaces existing) | [optional]
**is_opted_in** | Option<**bool**> | Opt-in status (changes are timestamped) | [optional]
**is_blocked** | Option<**bool**> | Block status | [optional]
**custom_fields** | Option<**std::collections::HashMap<String, String>**> | Custom fields to merge (set value to null to remove a field) | [optional]
**notes** | Option<**String**> | Notes about the contact | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


