# UpdateTrackingSiteRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | Option<**String**> |  | [optional]
**domains** | Option<**Vec<String>**> | Hosts allowed to send events, such as `brand.com`. Events from any other origin are dropped. | [optional]
**consent_mode** | Option<[**models::TrackingSiteConsentMode**](TrackingSiteConsentMode.md)> |  | [optional]
**custom_hostname** | Option<**String**> | A subdomain of one of the site's domains, never the domain itself. `null` removes it. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


