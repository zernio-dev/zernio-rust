# CreateAdSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id owning the Google Ads connection. | 
**platform** | **Platform** | Only \"google\" is implemented today; every other value returns 501. (enum: facebook, instagram, tiktok, linkedin, pinterest, google, twitter, openai) | 
**campaign_id** | **String** | Google platform campaign ID (numeric) the ad group is created under. | 
**name** | **String** |  | 
**status** | Option<**Status**> |  (enum: ACTIVE, PAUSED) | [optional][default to Paused]
**ad_account_id** | Option<**String**> | Platform ad account ID (Google customer ID, digits only). Only required when the connection has more than one. | [optional]
**customer_id** | Option<**String**> | Alias of adAccountId, kept for existing callers | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


