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

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


