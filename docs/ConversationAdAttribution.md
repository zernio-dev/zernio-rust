# ConversationAdAttribution

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ad_id** | Option<**String**> | Meta's ad ID: `meta_ad_id` on Instagram and Facebook, `ctwa_source_id` on WhatsApp when `ctwa_source_type` is `ad`. Accepted by `GET /v1/ads/{adId}`. | 
**name** | Option<**String**> | The synced ad's name, else the ad title or headline Meta sent. | 
**synced** | **bool** | True when the ad was found in your synced ads. | 
**campaign_id** | Option<**String**> | Meta campaign ID. Synced ads only. | 
**campaign_name** | Option<**String**> | Campaign name. Synced ads only. | 
**ad_set_id** | Option<**String**> | Meta ad set ID. Synced ads only. | 
**ad_set_name** | Option<**String**> | Ad set name. Synced ads only. | 
**ad_account_id** | Option<**String**> | Meta ad account ID (act_...). Synced ads only. | 
**ad_account_name** | Option<**String**> | Ad account name. Synced ads only. | 
**platform_post_id** | Option<**String**> | The post the ad promotes, from the synced ad or else Meta's `post_id` on the click. | 
**is_external** | Option<**bool**> | True when the ad was created outside Zernio (synced from Ads Manager), false when created through Zernio, null when not synced. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


