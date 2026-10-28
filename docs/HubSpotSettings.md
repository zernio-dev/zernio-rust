# HubSpotSettings

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | **String** | Zernio account ID of the HubSpot connection. | 
**platform** | **Platform** |  (enum: hubspot) | 
**hub_id** | **String** | HubSpot portal (hub) ID. | 
**hub_domain** | Option<**String**> | HubSpot portal domain, when HubSpot reports one. | 
**scopes** | **Vec<String>** | OAuth scopes the portal granted. | 
**sync_contacts** | **bool** | Whether Zernio creates HubSpot contacts for inbox contacts that match none. | 
**log_messages** | **bool** | Whether Zernio logs inbox messages on HubSpot contact timelines. | 
**report_deals** | **bool** | Whether Zernio sends closed-won deals as Purchase events to the profile's event destinations. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


