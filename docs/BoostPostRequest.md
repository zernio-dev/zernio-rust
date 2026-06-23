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
**bid_strategy** | Option<[**models::BidStrategy**](BidStrategy.md)> | Meta bid strategy applied to the ad set. On TikTok, mapped to `bid_type` / `bid_price` / `deep_bid_type` automatically.  | [optional]
**bid_amount** | Option<**f64**> | Bid cap in WHOLE currency units (USD: 5 = $5.00; JPY: 100 = ¥100). Required when `bidStrategy` is `LOWEST_COST_WITH_BID_CAP` or `COST_CAP`. Backward-compat: providing `bidAmount` without `bidStrategy` is treated as `LOWEST_COST_WITH_BID_CAP`.  | [optional]
**roas_average_floor** | Option<**f64**> | Minimum ROAS as a decimal multiplier (e.g. 2.0 = 2.0x ROAS). Required when `bidStrategy` is `LOWEST_COST_WITH_MIN_ROAS`. Sent to Meta as `bid_constraints.roas_average_floor` × 10000 (Meta uses fixed-point integers).  | [optional]
**tracking** | Option<[**models::BoostPostRequestTracking**](BoostPostRequestTracking.md)> |  | [optional]
**special_ad_categories** | Option<**Vec<SpecialAdCategories>**> | Meta only. Required for housing, employment, credit, or political ads. (enum: HOUSING, EMPLOYMENT, CREDIT, ISSUES_ELECTIONS_POLITICS) | [optional]
**link_url** | Option<**String**> | TikTok-only. Custom destination URL for the Spark Ad. Without this, TikTok Spark Ads have no clickable destination — required for traffic / conversion objectives. Maps to `landing_page_url` on the creative entry of /v2/ad/create/ (TikTok SDK `AdcreateCreatives.landing_page_url`). Ignored on Meta / LinkedIn / Pinterest / X / Google (those infer the destination from the boosted post).  | [optional]
**call_to_action** | Option<**String**> | TikTok-only. Call-to-action button label on the Spark Ad creative (e.g. `LEARN_MORE`, `SHOP_NOW`, `DOWNLOAD_NOW`, `SIGN_UP`, `WATCH_NOW`). Maps to `call_to_action` on the creative entry of /v2/ad/create/. Pass-through — the platform validates the value. See TikTok's \"Enumeration - Call-to-Action\" reference for the full list.  | [optional]
**spark_auth_code** | Option<**String**> | TikTok-only. Spark Code (creator's `auth_code`) authorizing cross-creator Spark Ads — the advertiser can boost a video owned by a DIFFERENT TikTok account. Without this, boosts are limited to videos owned by the same account running the ads (same-BC creators only). The creator generates the code in their TikTok app's Promote settings and shares it with the advertiser. Maps to `auth_code` on the creative entry of /v2/ad/create/.  | [optional]
**dsa_beneficiary** | Option<**String**> | Name of the legal entity benefiting from the ad. Required by Meta when targeting EU users (DSA Article 26). Not enforced at schema level; enforced server-side when targeting intersects EU member states.  | [optional]
**dsa_payor** | Option<**String**> | Name of the legal entity paying for the ad. Required by Meta when targeting EU users (DSA Article 26). Note Meta API spelling: dsa_payor (not dsa_payer).  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


