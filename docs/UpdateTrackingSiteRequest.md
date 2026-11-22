# UpdateTrackingSiteRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | Option<**String**> |  | [optional]
**pixels** | Option<[**Vec<models::TrackingSitePixel>**](TrackingSitePixel.md)> | The ad pixels the tag loads once consent allows, up to 20, one Microsoft UET tag at most. `null` or `[]` removes them. | [optional]
**consent_mode_bridge** | Option<**bool**> | Write the site's consent banner into Google Consent Mode v2: a denied default in the EEA, UK and Switzerland where the page sets none, then each update. | [optional]
**domains** | Option<**Vec<String>**> | Hosts allowed to send events, such as `brand.com`. Events from any other origin are dropped. | [optional]
**consent_mode** | Option<[**models::TrackingSiteConsentMode**](TrackingSiteConsentMode.md)> |  | [optional]
**custom_hostname** | Option<**String**> | A subdomain of one of the site's domains, never the domain itself. `null` removes it. | [optional]
**proxy_path** | Option<**String**> | The path your server forwards to the collector, such as `/zt`. `null` removes it. | [optional]
**google_tag_ids** | Option<**Vec<String>**> | Google tag ids such as `GTM-XXXXXXX`, `G-XXXXXXXXXX` or `AW-XXXXXXXXXX`, up to 10. `null` or `[]` removes them. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


