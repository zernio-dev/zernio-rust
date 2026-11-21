# CrmDeal

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**object_type** | **ObjectType** |  (enum: deal, opportunity) | 
**name** | Option<**String**> |  | 
**stage** | Option<**String**> | HubSpot stage id (`closedwon`), Salesforce `StageName` (`Closed Won`) or GoHighLevel pipeline stage id. A GoHighLevel opportunity's won or lost `status` is a native field (`properties=status`). | 
**amount** | Option<**f64**> |  | 
**currency** | Option<**String**> | ISO 4217. HubSpot sets it on multi-currency portals only. Salesforce gives the Opportunity's currency on multi-currency orgs, else the org currency read from its Currency Locale. Null on GoHighLevel. | 
**close_date** | Option<[**String**](String.md)> | Null on GoHighLevel, whose opportunities have no close date. | 
**owner_id** | Option<**String**> |  | 
**contact_ids** | **Vec<String>** | Associated HubSpot contacts, the Opportunity's contact roles (primary first), or the GoHighLevel opportunity's contact. | 
**created_at** | Option<**String**> |  | 
**updated_at** | Option<**String**> |  | 
**url** | **String** |  | 
**properties** | **std::collections::HashMap<String, serde_json::Value>** |  | 
**raw** | Option<**std::collections::HashMap<String, serde_json::Value>**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


