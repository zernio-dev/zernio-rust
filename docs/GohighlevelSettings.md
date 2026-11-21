# GohighlevelSettings

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | **String** |  | 
**platform** | **Platform** |  (enum: gohighlevel) | 
**location_id** | **String** | The GoHighLevel sub-account (location) id. | 
**company_id** | Option<**String**> | The agency that owns the sub-account, null for a sub-account under no agency. | 
**location_name** | Option<**String**> |  | 
**installed_by** | Option<**String**> | The GoHighLevel user who installed the app. | 
**relay_conversions** | **bool** | CRM events are relayed as conversions. Default true. | 
**write_back_attribution** | **bool** | Relayed conversions are written back onto the GoHighLevel contact. Default true. | 
**report_to_ads** | **bool** | Relayed conversions are forwarded to the profile's ad platforms. Default false. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


