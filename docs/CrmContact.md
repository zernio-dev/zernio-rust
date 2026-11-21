# CrmContact

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | The CRM's own id. | 
**object_type** | **ObjectType** | `lead` only on Salesforce. (enum: contact, lead) | 
**first_name** | Option<**String**> |  | 
**last_name** | Option<**String**> |  | 
**email** | Option<**String**> |  | 
**phone** | Option<**String**> | The phone, else the mobile phone, as stored in the CRM. | 
**company** | Option<**String**> | HubSpot `company`; Salesforce Lead `Company` or Contact Account name; GoHighLevel `companyName`. | 
**owner_id** | Option<**String**> |  | 
**created_at** | Option<**String**> |  | 
**updated_at** | Option<**String**> |  | 
**url** | **String** | Opens the record in the CRM. | 
**properties** | **std::collections::HashMap<String, serde_json::Value>** | The native fields asked for with `properties`, by name. | 
**raw** | Option<**std::collections::HashMap<String, serde_json::Value>**> | The CRM's own record, only with `includeRaw=true`. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


