# ConversionEventUserClickIds

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**fbc** | Option<**String**> | Meta click ID (from fbclid URL param). | [optional]
**fbp** | Option<**String**> | Meta browser ID (_fbp cookie). | [optional]
**gclid** | Option<**String**> | Google click ID (from gclid URL param). | [optional]
**gbraid** | Option<**String**> | Google iOS 14.5+ app attribution ID. | [optional]
**wbraid** | Option<**String**> | Google iOS 14.5+ web-to-app attribution ID. | [optional]
**li_fat_id** | Option<**String**> | LinkedIn first-party ad tracking click ID. Captured by parsing `li_fat_id` from landing-page URLs after the advertiser enables enhanced conversion tracking on the LinkedIn Insight Tag. Sent to LinkedIn as the LINKEDIN_FIRST_PARTY_ADS_TRACKING_UUID userId. Opaque token, not hashed.  | [optional]
**epik** | Option<**String**> | Pinterest click ID (the `epik` URL param or `_epik` cookie). Sent to Pinterest as `click_id`, not hashed. | [optional]
**rdt_cid** | Option<**String**> | Reddit click ID (the `rdt_cid` URL param Reddit adds to ad clicks). Sent to Reddit as `click_id`, not hashed. | [optional]
**rdt_uuid** | Option<**String**> | Reddit Pixel browser id (the `_rdt_uuid` first-party cookie). Sent to Reddit as `user.uuid`, not hashed. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


