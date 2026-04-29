# Ad

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**platform** | Option<**Platform**> |  (enum: facebook, instagram, tiktok, linkedin, pinterest, google, twitter) | [optional]
**status** | Option<[**models::AdStatus**](AdStatus.md)> |  | [optional]
**ad_type** | Option<**AdType**> |  (enum: boost, standalone) | [optional]
**goal** | Option<**Goal**> | Available goals vary by platform. Meta (Facebook/Instagram) and TikTok support all 7. LinkedIn supports all except app_promotion. Twitter/X supports engagement, traffic, awareness, video_views, app_promotion. Pinterest and Google Ads support only engagement, traffic, awareness, video_views. (enum: engagement, traffic, awareness, video_views, lead_generation, conversions, app_promotion) | [optional]
**is_external** | Option<**bool**> | True for ads synced from platform ad managers | [optional]
**budget** | Option<[**models::AdBudget**](AdBudget.md)> |  | [optional]
**metrics** | Option<[**models::AdMetrics**](AdMetrics.md)> |  | [optional]
**platform_ad_id** | Option<**String**> |  | [optional]
**platform_ad_account_id** | Option<**String**> |  | [optional]
**platform_campaign_id** | Option<**String**> |  | [optional]
**platform_ad_set_id** | Option<**String**> |  | [optional]
**campaign_name** | Option<**String**> |  | [optional]
**ad_set_name** | Option<**String**> |  | [optional]
**platform_objective** | Option<**String**> | Raw Meta campaign objective (e.g. OUTCOME_SALES, OUTCOME_LEADS, OUTCOME_TRAFFIC). Only present for Meta ads. | [optional]
**optimization_goal** | Option<**String**> | Meta ad set optimization goal (e.g. OFFSITE_CONVERSIONS, VALUE, LEAD_GENERATION, LINK_CLICKS). Only present for Meta ads. | [optional]
**platform_ad_account_name** | Option<**String**> | Human-readable advertiser/account name (Meta `AdAccount.name`, TikTok `advertiser_name`, LinkedIn / X / Pinterest equivalents). Refreshed every sync so platform-side renames propagate within one cycle. `null` when the platform doesn't return a name or the sync hasn't run yet.  | [optional]
**platform_created_at** | Option<**String**> | Platform-reported creation timestamp (Meta `created_time`, TikTok `create_time`). Distinct from `createdAt` which reflects when Zernio first synced the doc — for sort/filter by \"when the ad was actually created on the platform\", read this field. `null` for legacy ads synced before this field was added; aggregations fall back to `createdAt` in that case.  | [optional]
**bid_strategy** | Option<[**models::BidStrategy**](BidStrategy.md)> | Ad-set bid strategy (overrides campaign level on Meta). Populated for Meta and TikTok. TikTok's native `bid_type` is normalized to the cross-platform Meta enum: `BID_TYPE_NO_BID` -> `LOWEST_COST_WITHOUT_CAP`, `BID_TYPE_CUSTOM` -> `LOWEST_COST_WITH_BID_CAP`, deep_bid_type=MIN_ROAS or roas_bid>0 -> `LOWEST_COST_WITH_MIN_ROAS`, `BID_TYPE_MAX_CONVERSION` -> `LOWEST_COST_WITHOUT_CAP`.  | [optional]
**bid_amount** | Option<**f64**> | Bid cap in WHOLE currency units of the ad account (USD: 5 = $5.00; JPY: 100 = ¥100). Populated when bidStrategy is `LOWEST_COST_WITH_BID_CAP` or `COST_CAP`. `null` for auto-bid (`LOWEST_COST_WITHOUT_CAP`).  - Meta source: `bid_amount` on the ad set (smallest-denomination int, decoded here). - TikTok source: priority order `bid_price` -> `conversion_bid_price` -> `deep_cpa_bid`   (whichever is set on the ad group). TikTok stores all three in whole currency units.  Source: facebook-business-sdk-codegen api_specs/specs/AdSet.json (`bid_amount`).  | [optional]
**roas_average_floor** | Option<**f64**> | Minimum ROAS as a decimal multiplier (2.0 = 2.0x ROAS). Populated when bidStrategy is `LOWEST_COST_WITH_MIN_ROAS`.  - Meta source: decoded from `bid_constraints.roas_average_floor` (Meta stores as   fixed-point int × 10000; we return the decimal). - TikTok source: `roas_bid` on the ad group (already a decimal).  Source: facebook-business-sdk-codegen api_specs/specs/AdCampaignBidConstraint.json.  | [optional]
**promoted_object** | Option<[**models::AdPromotedObject**](AdPromotedObject.md)> |  | [optional]
**creative** | Option<[**models::AdCreative**](AdCreative.md)> |  | [optional]
**targeting** | Option<**serde_json::Value**> |  | [optional]
**schedule** | Option<[**models::AdSchedule**](AdSchedule.md)> |  | [optional]
**rejection_reason** | Option<**String**> |  | [optional]
**created_at** | Option<**String**> |  | [optional]
**updated_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


