# CreateAdCampaignRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. | 
**ad_account_id** | **String** | Meta ad account id (act_<n>). | 
**name** | **String** |  | 
**goal** | **Goal** | Mapped to the ODAX objective (same mapping as POST /v1/ads/create). (enum: engagement, traffic, awareness, video_views, lead_generation, lead_conversion, job_applicants, conversions, app_promotion, catalog_sales) | 
**special_ad_categories** | Option<**Vec<SpecialAdCategories>**> |  (enum: HOUSING, EMPLOYMENT, CREDIT, ISSUES_ELECTIONS_POLITICS, FINANCIAL_PRODUCTS_SERVICES, ONLINE_GAMBLING_AND_GAMING) | [optional]
**budget_amount** | Option<**f64**> | Campaign-level (CBO) budget in whole currency units. Requires budgetType. | [optional]
**budget_type** | Option<**BudgetType**> |  (enum: daily, lifetime) | [optional]
**status** | Option<**Status**> |  (enum: ACTIVE, PAUSED) | [optional][default to Paused]
**bid_strategy** | Option<**BidStrategy**> | Campaign bid strategy. Meta puts `bid_strategy` where the budget lives, so this applies only alongside a campaign budget (CBO). Previously settable only via `PUT /v1/ads/campaigns/{campaignId}`. (enum: LOWEST_COST_WITHOUT_CAP, LOWEST_COST_WITH_BID_CAP, COST_CAP, LOWEST_COST_WITH_MIN_ROAS) | [optional]
**bid_amount** | Option<**f64**> | Whole currency units (USD: 5 = $5.00). Required for LOWEST_COST_WITH_BID_CAP and COST_CAP; ignored otherwise. | [optional]
**roas_average_floor** | Option<**f64**> | Decimal ROAS multiplier (2.0 = 2.0x). Required for LOWEST_COST_WITH_MIN_ROAS. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


