# CreateAdCampaignRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. | 
**ad_account_id** | **String** | Meta ad account id (act_<n>). | 
**name** | **String** |  | 
**goal** | **Goal** | Mapped to the ODAX objective (same mapping as POST /v1/ads/create). (enum: engagement, traffic, awareness, video_views, lead_generation, lead_conversion, job_applicants, conversions, app_promotion, catalog_sales) | 
**special_ad_categories** | Option<**Vec<SpecialAdCategories>**> |  (enum: HOUSING, EMPLOYMENT, CREDIT, ISSUES_ELECTIONS_POLITICS, FINANCIAL_PRODUCTS_SERVICES, ONLINE_GAMBLING_AND_GAMING) | [optional]
**budget_amount** | Option<**f64**> | Campaign-level (CBO) budget in WHOLE currency units (USD: 50 = $50.00), NOT cents — Meta's own Marketing API takes this same number in minor units, so it is an easy and expensive mix-up. Requires budgetType. | [optional]
**budget_type** | Option<**BudgetType**> |  (enum: daily, lifetime) | [optional]
**status** | Option<**Status**> |  (enum: ACTIVE, PAUSED) | [optional][default to Paused]
**bid_strategy** | Option<**BidStrategy**> | Campaign bid strategy. Meta stores `bid_strategy` alongside the budget, so this REQUIRES `budgetAmount` + `budgetType` on the same request; sending it without a campaign budget is a 400. A campaign carrying a strategy without its `bid_amount` makes every ad set created under it fail with an error that names the ad set (code 100, subcode 1815857), so the bad state is rejected up front rather than accepted. To bid at ad-set level, set the strategy there instead. (enum: LOWEST_COST_WITHOUT_CAP, LOWEST_COST_WITH_BID_CAP, COST_CAP, LOWEST_COST_WITH_MIN_ROAS) | [optional]
**bid_amount** | Option<**f64**> | Whole currency units (USD: 5 = $5.00). Required for LOWEST_COST_WITH_BID_CAP and COST_CAP; ignored otherwise. Validated here but NOT stored by Meta: the campaign object has no bid_amount field, only bid_strategy lives on it. The amount takes effect once an ad set joins this campaign (existingCampaignId on POST /v1/ads/create) and supplies its own bidAmount there. | [optional]
**roas_average_floor** | Option<**f64**> | Decimal ROAS multiplier (2.0 = 2.0x). Required for LOWEST_COST_WITH_MIN_ROAS. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


