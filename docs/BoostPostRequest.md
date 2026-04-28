# BoostPostRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**post_id** | Option<**String**> | Zernio post ID (provide this or platformPostId) | [optional]
**platform_post_id** | Option<**String**> | Platform post ID (alternative to postId) | [optional]
**account_id** | **String** | Social account ID | 
**ad_account_id** | **String** | Platform ad account ID | 
**name** | **String** |  | 
**goal** | **Goal** | Available goals vary by platform. Meta (Facebook/Instagram) and TikTok support all 7. LinkedIn supports all except app_promotion. Twitter/X supports engagement, traffic, awareness, video_views, app_promotion. Pinterest and Google Ads support only engagement, traffic, awareness, video_views. (enum: engagement, traffic, awareness, video_views, lead_generation, conversions, app_promotion) | 
**budget** | [**models::BoostPostRequestBudget**](BoostPostRequestBudget.md) |  | 
**currency** | Option<**String**> |  | [optional]
**schedule** | Option<[**models::BoostPostRequestSchedule**](BoostPostRequestSchedule.md)> |  | [optional]
**targeting** | Option<[**models::BoostPostRequestTargeting**](BoostPostRequestTargeting.md)> |  | [optional]
**bid_amount** | Option<**f64**> | Max bid cap (Meta only) | [optional]
**tracking** | Option<[**models::BoostPostRequestTracking**](BoostPostRequestTracking.md)> |  | [optional]
**special_ad_categories** | Option<**Vec<SpecialAdCategories>**> | Meta only. Required for housing, employment, credit, or political ads. (enum: HOUSING, EMPLOYMENT, CREDIT, ISSUES_ELECTIONS_POLITICS) | [optional]
**dsa_beneficiary** | Option<**String**> | Name of the legal entity benefiting from the ad. Required by Meta when targeting EU users (DSA Article 26). Not enforced at schema level; enforced server-side when targeting intersects EU member states.  | [optional]
**dsa_payor** | Option<**String**> | Name of the legal entity paying for the ad. Required by Meta when targeting EU users (DSA Article 26). Note Meta API spelling: dsa_payor (not dsa_payer).  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


