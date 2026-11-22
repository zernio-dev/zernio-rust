# GohighlevelFunnelTracking

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**site_id** | **String** | The Zernio tracking site behind the tag (`getTrackingSite`). | 
**snippet** | **String** | The line to paste into each funnel's and website's tracking code (Header). | 
**live** | **bool** | The tag has sent its first visit. | 
**domains** | **Vec<String>** | The domains whose visits are tied to contacts. A page checked with `verifyGohighlevelFunnelTracking` adds its domain. | 
**funnels** | [**Vec<models::GohighlevelFunnelTrackingFunnelsInner>**](GohighlevelFunnelTrackingFunnelsInner.md) |  | 
**verified** | [**models::GohighlevelFunnelTrackingVerified**](GohighlevelFunnelTrackingVerified.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


