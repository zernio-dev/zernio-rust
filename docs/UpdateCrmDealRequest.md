# UpdateCrmDealRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | Option<**String**> |  | [optional]
**stage** | Option<**String**> | HubSpot stage id, Salesforce `StageName` or GoHighLevel pipeline stage id. | [optional]
**amount** | Option<**f64**> |  | [optional]
**currency** | Option<**String**> | ISO 4217 code. Multi-currency HubSpot portals and Salesforce orgs only. | [optional]
**close_date** | Option<[**String**](String.md)> |  | [optional]
**owner_id** | Option<**String**> | An id from `GET /v1/crm/{accountId}/owners`. | [optional]
**properties** | Option<[**std::collections::HashMap<String, models::CrmNativePropertiesValue>**](CrmNativePropertiesValue.md)> | Native fields by internal name (HubSpot `lifecyclestage`, Salesforce `LeadSource` or `Industry__c`). On GoHighLevel, a record field (`source`, an opportunity `status`) or else a custom field id or key. A unified field of the same request wins over its native twin. `null` clears a field. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


