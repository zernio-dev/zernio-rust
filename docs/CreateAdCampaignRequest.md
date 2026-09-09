# CreateAdCampaignRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant); its platform decides where the campaign is created. | 
**ad_account_id** | **String** | Platform ad account id (Meta act_<n>, Google customer id, LinkedIn account id, ...). | 
**name** | **String** |  | 
**goal** | **Goal** | Mapped to the ODAX objective (same mapping as POST /v1/ads/create). (enum: engagement, traffic, awareness, video_views, lead_generation, lead_conversion, job_applicants, conversions, app_promotion, catalog_sales, page_likes) | 
**is_skadnetwork_attribution** | Option<**bool**> | Meta app promotion only. Immutable campaign flag. Set true for iOS 14+ SKAdNetwork campaigns and supply promotedObject.applicationId plus promotedObject.objectStoreUrl. The campaign receives promotedObject only when this flag is true. Cannot be changed on an existing campaign. | [optional]
**promoted_object** | Option<[**models::AdPromotedObject**](AdPromotedObject.md)> |  | [optional]
**buying_type** | Option<**BuyingType**> | Meta only. SKAdNetwork app promotion requires AUCTION. (enum: AUCTION, RESERVED) | [optional]
**validate_only** | Option<**bool**> | Meta only. Runs campaign validation without creating or persisting a campaign; Idempotency-Key storage is bypassed. Returns HTTP 200 with validateOnly true and status VALIDATED. | [optional]
**special_ad_categories** | Option<**Vec<SpecialAdCategories>**> |  (enum: HOUSING, EMPLOYMENT, CREDIT, ISSUES_ELECTIONS_POLITICS, FINANCIAL_PRODUCTS_SERVICES, ONLINE_GAMBLING_AND_GAMING) | [optional]
**budget_amount** | Option<**f64**> | Campaign-level (CBO) budget in WHOLE currency units (USD: 50 = $50.00), NOT cents. Meta's own Marketing API takes this same number in minor units, so it is an easy and expensive mix-up. Requires budgetType. | [optional]
**budget_type** | Option<**BudgetType**> |  (enum: daily, lifetime) | [optional]
**status** | Option<**Status**> |  (enum: ACTIVE, PAUSED) | [optional][default to Paused]
**bid_strategy** | Option<**BidStrategy**> | Campaign bid strategy. Meta stores `bid_strategy` alongside the budget, so this REQUIRES `budgetAmount` + `budgetType` on the same request; sending it without a campaign budget is a 400. A campaign carrying a strategy without its `bid_amount` makes every ad set created under it fail with an error that names the ad set (code 100, subcode 1815857), so the bad state is rejected up front rather than accepted. To bid at ad-set level on Meta, set the strategy there instead. On Google: LOWEST_COST_WITHOUT_CAP = Maximize Conversions, COST_CAP + bidAmount = Target CPA, LOWEST_COST_WITH_MIN_ROAS + roasAverageFloor = Target ROAS, LOWEST_COST_WITH_BID_CAP + bidAmount = Maximize Clicks with a CPC ceiling; portfolioBidStrategyId attaches a portfolio strategy instead. (enum: LOWEST_COST_WITHOUT_CAP, LOWEST_COST_WITH_BID_CAP, COST_CAP, LOWEST_COST_WITH_MIN_ROAS) | [optional]
**bid_amount** | Option<**f64**> | Whole currency units (USD: 5 = $5.00). Required for LOWEST_COST_WITH_BID_CAP and COST_CAP; ignored otherwise. On Meta, validated here but NOT stored: the campaign object has no bid_amount field, only bid_strategy lives on it, and the amount takes effect once an ad set joins this campaign (existingCampaignId on POST /v1/ads/create) and supplies its own bidAmount there. On Google, stored directly on the campaign's bidding strategy. | [optional]
**roas_average_floor** | Option<**f64**> | Decimal ROAS multiplier (2.0 = 2.0x). Required for LOWEST_COST_WITH_MIN_ROAS. | [optional]
**portfolio_bid_strategy_id** | Option<**String**> | Google only. Attach an existing portfolio bid strategy (numeric id from GET /v1/ads/bid-strategies) to the new campaign instead of a standard one. Exclusive with bidStrategy. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


