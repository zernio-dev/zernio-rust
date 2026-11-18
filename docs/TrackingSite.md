# TrackingSite

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**profile_id** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**status** | Option<**Status**> |  (enum: active, paused, removing) | [optional]
**install** | Option<[**models::TrackingSiteInstall**](TrackingSiteInstall.md)> |  | [optional]
**store_orders** | Option<**bool**> | True when the store's orders reach Zernio from the store itself, so website purchases are forwarded but not counted twice. | [optional]
**site_key** | Option<**String**> | Public key that names the site in the snippet, such as `zs_...`. | [optional]
**domains** | Option<**Vec<String>**> |  | [optional]
**custom_hostname** | Option<[**models::TrackingSiteCustomHostname**](TrackingSiteCustomHostname.md)> |  | [optional]
**proxy** | Option<[**models::TrackingSiteProxy**](TrackingSiteProxy.md)> |  | [optional]
**google_tag_ids** | Option<**Vec<String>**> | The site's own Google tags (Tag Manager, GA4, Google Ads) its own-domain path relays to Google, so they load and measure from the site's domain. | [optional]
**consent_mode** | Option<[**models::TrackingSiteConsentMode**](TrackingSiteConsentMode.md)> |  | [optional]
**checks** | Option<[**Vec<models::TrackingSiteChecksInner>**](TrackingSiteChecksInner.md)> | One per setup step: `script` for the install, then one per ad account the site sends to, keyed by its platform and ids. | [optional]
**setup** | Option<[**models::TrackingSiteSetup**](TrackingSiteSetup.md)> |  | [optional]
**created_at** | Option<**String**> |  | [optional]
**updated_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


