# UpdateCreatorCampaignRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | Option<**String**> |  | [optional]
**brand_name** | Option<**String**> |  | [optional]
**platforms** | Option<**Vec<Platforms>**> |  (enum: tiktok, instagram, youtube, threads, pinterest, facebook, twitter) | [optional]
**content_rules** | Option<**String**> |  | [optional]
**starts_at** | Option<**String**> |  | [optional]
**ends_at** | Option<**String**> |  | [optional]
**tracking_days** | Option<**i32**> |  | [optional]
**hold_days** | Option<**i32**> |  | [optional]
**max_post_age_minutes** | Option<**i32**> | Null removes the limit. | [optional]
**settlement** | Option<**Settlement**> |  (enum: none, external, treasury) | [optional]
**economics** | Option<[**models::CreatorCampaignEconomics**](CreatorCampaignEconomics.md)> |  | [optional]
**caps** | Option<[**models::CreatorCampaignCaps**](CreatorCampaignCaps.md)> |  | [optional]
**branding** | Option<[**models::CreatorCampaignBranding**](CreatorCampaignBranding.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


