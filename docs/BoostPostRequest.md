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
**raw_targeting** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Meta only. A Meta-native targeting spec (e.g. `{ \"geo_locations\": { \"cities\": [{ \"key\": \"...\", \"radius\": 15, \"distance_unit\": \"kilometer\" }] } }`). Sent alone it is forwarded unchanged. Use for advanced fields the structured object does not expose (flexible_spec, excluded audiences, business places, user_os, wireless_carrier).  Can be combined with `targeting`: rawTargeting is the BASE layer and the built camelCase spec is merged on top, key by key (camelCase wins on collision). The merge goes one level deep inside `geo_locations` and `excluded_geo_locations` (built sub-keys win; raw-only sub-keys such as `location_types` survive). Array values (`flexible_spec`, ...) are replaced as a whole key, never element-merged.  When `rawTargeting` is present the `advantage_audience: 0` default that Zernio normally applies is no longer emitted, so it cannot clobber a `targeting_automation` sent in the raw spec. Meta requires `targeting_automation` on ad set creation, so include it in the raw spec, or send `targeting.advantage_audience` (0 or 1), which is merged over raw as `targeting_automation`.  | [optional]
**bid_strategy** | Option<[**models::BidStrategy**](BidStrategy.md)> | Meta bid strategy applied to the ad set. On TikTok, mapped to `bid_type` / `bid_price` / `deep_bid_type` automatically.  | [optional]
**bid_amount** | Option<**f64**> | Bid cap in WHOLE currency units (USD: 5 = $5.00; JPY: 100 = ¥100). Required when `bidStrategy` is `LOWEST_COST_WITH_BID_CAP` or `COST_CAP`. Backward-compat: providing `bidAmount` without `bidStrategy` is treated as `LOWEST_COST_WITH_BID_CAP`.  | [optional]
**roas_average_floor** | Option<**f64**> | Minimum ROAS as a decimal multiplier (e.g. 2.0 = 2.0x ROAS). Required when `bidStrategy` is `LOWEST_COST_WITH_MIN_ROAS`. Sent to Meta as `bid_constraints.roas_average_floor` × 10000 (Meta uses fixed-point integers).  | [optional]
**platform_specific_data** | Option<[**models::LinkedInAdsPlatformData**](LinkedInAdsPlatformData.md)> |  | [optional]
**tracking** | Option<[**models::BoostPostRequestTracking**](BoostPostRequestTracking.md)> |  | [optional]
**special_ad_categories** | Option<**Vec<SpecialAdCategories>**> | Meta only. Required for housing, employment, credit, or political ads. (enum: HOUSING, EMPLOYMENT, CREDIT, FINANCIAL_PRODUCTS_SERVICES, ISSUES_ELECTIONS_POLITICS, ONLINE_GAMBLING_AND_GAMING) | [optional]
**special_ad_category_country** | Option<**Vec<String>**> | Meta (metaads) only. 2-letter ISO country codes the special ad category applies to. Requires specialAdCategories to be set (400 otherwise). | [optional]
**link_url** | Option<**String**> | TikTok-only. Custom destination URL for the Spark Ad. Without this, TikTok Spark Ads have no clickable destination — required for traffic / conversion objectives. Maps to `landing_page_url` on the creative entry of /v2/ad/create/ (TikTok SDK `AdcreateCreatives.landing_page_url`). Ignored on Meta / LinkedIn / Pinterest / X / Google (those infer the destination from the boosted post).  | [optional]
**call_to_action** | Option<**String**> | TikTok-only. Call-to-action button label on the Spark Ad creative (e.g. `LEARN_MORE`, `SHOP_NOW`, `DOWNLOAD_NOW`, `SIGN_UP`, `WATCH_NOW`). Maps to `call_to_action` on the creative entry of /v2/ad/create/. Pass-through — the platform validates the value. See TikTok's \"Enumeration - Call-to-Action\" reference for the full list.  | [optional]
**spark_auth_code** | Option<**String**> | TikTok-only. Spark Code (creator's `auth_code`) authorizing cross-creator Spark Ads — the advertiser can boost a video owned by a DIFFERENT TikTok account. Without this, boosts are limited to videos owned by the same account running the ads (same-BC creators only). The creator generates the code in their TikTok app's Promote settings and shares it with the advertiser. Maps to `auth_code` on the creative entry of /v2/ad/create/.  | [optional]
**dsa_beneficiary** | Option<**String**> | Legal entity that benefits from the ad. Required when targeting EU users (EU DSA, Article 26). Optional if the ad account has a default beneficiary: set it once via `PATCH /v1/ads/accounts` or in Meta Ads Manager, and Meta fills it in whenever the field is omitted.  | [optional]
**dsa_payor** | Option<**String**> | Legal entity that pays for the ad. Can differ from `dsaBeneficiary` (for example, an agency paying for a client's ads). Same rules as `dsaBeneficiary`: required for EU targeting unless the ad account has a default payor.  | [optional]
**optimization_goal** | Option<**String**> | Meta only. Explicit ad-set `optimization_goal` override. When omitted, defaults to the value derived from `goal`. The value must be compatible with the objective Meta derives from `goal`, not with the objective used by `POST /v1/ads/create` for the same `goal` name: boost maps `goal: \"engagement\"` to objective `OUTCOME_AWARENESS`, which accepts `REACH`, `IMPRESSIONS`, `AD_RECALL_LIFT`, or THRUPLAY-class values, and rejects `POST_ENGAGEMENT` (that value is only valid under `OUTCOME_ENGAGEMENT`, which create uses for the same goal name).  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


