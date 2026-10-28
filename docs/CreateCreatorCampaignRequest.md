# CreateCreatorCampaignRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** | Profile the campaign lives in. Creator accounts connect into the same workspace. | 
**name** | **String** |  | 
**brand_name** | **String** |  | 
**economics** | [**models::CreatorCampaignEconomics**](CreatorCampaignEconomics.md) |  | 
**caps** | Option<[**models::CreatorCampaignCaps**](CreatorCampaignCaps.md)> |  | [optional][default to {authenticityThreshold=40}]
**platforms** | Option<**Vec<Platforms>**> | Platforms creators may post on. At least one is needed to activate. (enum: tiktok, instagram, youtube) | [optional]
**content_rules** | Option<**String**> |  | [optional]
**starts_at** | Option<**String**> |  | [optional]
**ends_at** | Option<**String**> |  | [optional]
**tracking_days** | Option<**i32**> |  | [optional][default to 30]
**hold_days** | Option<**i32**> |  | [optional][default to 10]
**max_post_age_minutes** | Option<**i32**> |  | [optional][default to 60]
**settlement** | Option<**Settlement**> |  (enum: none, external, treasury) | [optional][default to None]
**branding** | Option<[**models::CreatorCampaignBranding**](CreatorCampaignBranding.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


