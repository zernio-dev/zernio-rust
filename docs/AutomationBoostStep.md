# AutomationBoostStep

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**r#type** | **Type** |  (enum: ads.boost_post) | 
**ad_account_id** | **String** | The Meta ad account that pays, from `GET /v1/ads/accounts`. | 
**budget** | **f64** | The whole spend of one boost, in the ad account currency. | 
**days** | **i32** | How long each boost runs. | 
**goal** | Option<**Goal**> |  (enum: engagement, awareness, video_views) | [optional][default to Engagement]
**countries** | **Vec<String>** | ISO 3166 alpha-2 codes. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


