# CrmContactInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**first_name** | Option<**String**> |  | [optional]
**last_name** | Option<**String**> |  | [optional]
**email** | Option<**String**> |  | [optional]
**phone** | Option<**String**> |  | [optional]
**company** | Option<**String**> |  | [optional]
**owner_id** | Option<**String**> | An id from `GET /v1/crm/{accountId}/owners`. | [optional]
**properties** | Option<[**std::collections::HashMap<String, models::CrmNativePropertiesValue>**](CrmNativePropertiesValue.md)> | Native fields by internal name (HubSpot `lifecyclestage`, Salesforce `LeadSource` or `Industry__c`). A unified field of the same request wins over its native twin. `null` clears a field. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


