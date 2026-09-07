# CreateAdSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id owning the Google Ads connection. | 
**platform** | **Platform** | Only \"google\" is implemented today; every other value returns 501. (enum: facebook, instagram, tiktok, linkedin, pinterest, google, twitter, openai) | 
**campaign_id** | **String** | Google platform campaign ID (numeric) the ad group is created under. | 
**name** | **String** |  | 
**status** | Option<**Status**> |  (enum: ACTIVE, PAUSED) | [optional][default to Paused]
**customer_id** | Option<**String**> | Numeric Google Ads customer id. Only required when the connection has more than one. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


