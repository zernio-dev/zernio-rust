# CreateAdSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id owning the Google Ads connection. | 
**platform** | **Platform** | Only \"google\" is implemented today; every other value returns 501. (enum: facebook, instagram, tiktok, linkedin, pinterest, google, twitter, openai) | 
**campaign_id** | **String** | Google platform campaign ID (numeric) the ad group is created under. | 
**name** | **String** |  | 
**status** | Option<**Status**> |  (enum: ACTIVE, PAUSED) | [optional][default to Paused]
**max_cpc** | Option<**f64**> | Max CPC of the new ad group, in the account's currency units. Send it when the campaign uses Manual CPC: Google gives an ad group without one a 0.01 bid. | [optional]
**ad_account_id** | Option<**String**> | Platform ad account ID (Google customer ID, digits only). Only required when the connection has more than one. | [optional]
**customer_id** | Option<**String**> | Alias of adAccountId, kept for existing callers | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


