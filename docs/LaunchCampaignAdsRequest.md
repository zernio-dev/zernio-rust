# LaunchCampaignAdsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**submission_ids** | **Vec<String>** | Approved submissions to run as ads. | 
**network** | **Network** | Meta runs Instagram and Facebook posts; TikTok runs TikTok posts. (enum: meta, tiktok) | 
**account_id** | **String** | The brand's connected ads account (Facebook or TikTok) the ads run from, as in `/v1/accounts`. | 
**ad_account_id** | **String** | Platform ad account ID. | 
**ad_set_id** | Option<**String**> | Existing Meta ad set the ads go into. Required when `network` is `meta`. | [optional]
**existing_campaign_id** | Option<**String**> | Existing TikTok campaign that gets one ad group per post. Required when `network` is `tiktok`. | [optional]
**daily_budget** | Option<**f64**> | Daily budget of each TikTok ad group, in the ad account currency. Required when `network` is `tiktok`. | [optional]
**identity** | **Identity** | Whose handle the ad runs under. TikTok takes `creator` only. (enum: brand, creator) | 
**body** | Option<**String**> | Primary text of brand ads. Defaults to the post caption. | [optional]
**headline** | Option<**String**> |  | [optional]
**call_to_action** | Option<**String**> | Call to action, as in `POST /v1/ads/create`. | [optional]
**link_url** | Option<**String**> | Destination URL (http or https). | [optional]
**status** | Option<**Status**> | Ads launch paused unless set to `ACTIVE`. (enum: ACTIVE, PAUSED) | [optional][default to Paused]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


