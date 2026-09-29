# UpsertCommerceMarketingActivityRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** |  | 
**remote_id** | **String** |  | 
**title** | **String** |  | 
**url** | **String** |  | 
**preview_image_url** | Option<**String**> |  | [optional]
**utm** | Option<[**models::UpsertCommerceMarketingActivityRequestUtm**](UpsertCommerceMarketingActivityRequestUtm.md)> |  | [optional]
**tactic** | **Tactic** |  (enum: ad, post, message, newsletter, link, affiliate, retargeting, loyalty, seo) | 
**channel** | **Channel** |  (enum: social, search, display, email, referral) | 
**status** | **Status** |  (enum: active, inactive, paused, scheduled) | 
**budget** | Option<[**models::UpsertCommerceMarketingActivityRequestBudget**](UpsertCommerceMarketingActivityRequestBudget.md)> |  | [optional]
**ad_spend** | Option<**String**> | Decimal in the store currency. | [optional]
**started_at** | Option<**String**> |  | [optional]
**ended_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


