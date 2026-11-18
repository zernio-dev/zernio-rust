# UpdateTrackingSiteRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | Option<**String**> |  | [optional]
**domains** | Option<**Vec<String>**> | Hosts allowed to send events, such as `brand.com`. Events from any other origin are dropped. | [optional]
**consent_mode** | Option<[**models::TrackingSiteConsentMode**](TrackingSiteConsentMode.md)> |  | [optional]
**custom_hostname** | Option<**String**> | A subdomain of one of the site's domains, never the domain itself. `null` removes it. | [optional]
**proxy_path** | Option<**String**> | The path your server forwards to the collector, such as `/zt`. `null` removes it. | [optional]
**google_tag_ids** | Option<**Vec<String>**> | Google tag ids such as `GTM-XXXXXXX`, `G-XXXXXXXXXX` or `AW-XXXXXXXXXX`, up to 10. `null` or `[]` removes them. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


