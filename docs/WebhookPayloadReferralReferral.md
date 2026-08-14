# WebhookPayloadReferralReferral

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#ref** | Option<**String**> | The `ref` parameter of the clicked ig.me / m.me link or ad. | [optional]
**source** | Option<**String**> | Meta-supplied source (`SHORTLINK`, `SHORTLINKS`, `IGME-SOURCE-LINK`, `ADS` - treat as opaque). | [optional]
**r#type** | Option<**String**> | Meta-supplied referral type (e.g. `OPEN_THREAD`). | [optional]
**referer_uri** | Option<**String**> | URI of the originating site, when Meta supplies one. Facebook Messenger only. | [optional]
**ad_id** | Option<**String**> | The Meta ad ID, on returning ad clicks. Facebook Messenger only. | [optional]
**ads_context_data** | Option<[**models::WebhookPayloadReferralReferralAdsContextData**](WebhookPayloadReferralReferralAdsContextData.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


