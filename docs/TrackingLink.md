# TrackingLink

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**code** | Option<**String**> | The short code in `url`, such as `aB3dE5fG`. Unique across Zernio. | [optional]
**site_id** | Option<**String**> | The tracking site the link belongs to. | [optional]
**profile_id** | Option<**String**> |  | [optional]
**status** | Option<**Status**> |  (enum: active, paused) | [optional]
**destinations** | Option<[**Vec<models::TrackingLinkDestination>**](TrackingLinkDestination.md)> |  | [optional]
**campaign** | Option<[**models::TrackingLinkCampaign**](TrackingLinkCampaign.md)> |  | [optional]
**url** | Option<**String**> | The link to put in ads, such as `https://t.brand.com/r/aB3dE5fG`. It uses the site's custom subdomain once that is active. | [optional]
**postback_url** | Option<**String**> | The server-to-server postback URL to give the network. Replace `{clickid}`, `{payout}` and `{txid}` with the network's own macros. It holds a secret: rotate it with `POST /v1/tracking-links/{linkId}/rotate-postback-token` if it leaks. | [optional]
**created_at** | Option<**String**> |  | [optional]
**updated_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


