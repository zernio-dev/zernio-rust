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
**log_delivery_status** | **bool** | Whether Zernio keeps the delivery status (sent, delivered, read, played, failed) of logged outgoing messages up to date on their HubSpot timeline entries. Only applies while `logMessages` is on. Defaults to `true`. | 
**report_deals** | **bool** | Whether Zernio sends closed-won deals as Purchase events to the profile's event destinations. | 
**use_deals_as_results** | **bool** | Whether closed-won deals count as sales on the ad campaign that brought their contact, in campaign results and ad rules. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


