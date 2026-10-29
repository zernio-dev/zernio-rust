# CreatorPortalCampaign

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | The campaign id, as in a link-recovery URL. | 
**name** | **String** |  | 
**brand_name** | **String** |  | 
**logo_url** | Option<**String**> |  | 
**theme** | Option<**serde_json::Value**> | Same keys as the `welcomeTheme` parameter of `GET /v1/connect/{platform}`. | 
**status** | **Status** |  (enum: draft, active, paused, closed) | 
**platforms** | **Vec<String>** |  | 
**content_rules** | Option<**String**> |  | 
**starts_at** | Option<**String**> |  | 
**ends_at** | Option<**String**> |  | 
**currency** | **String** |  | 
**economics** | [**models::CreatorPortalEconomics**](CreatorPortalEconomics.md) |  | 
**max_post_age_minutes** | Option<**i32**> | A post must be submitted within this many minutes of publishing. Null means any age. Either way, only posts published after the campaign started are accepted. | 
**hold_days** | **i32** | Days approved earnings stay owed before they become payable. | 
**tracking_days** | **i32** | Days each submitted post is tracked for views. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


