# CreateStandaloneAdRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** |  | 
**ad_account_id** | **String** |  | 
**name** | **String** |  | 
**goal** | Option<**Goal**> | Required on legacy + multi-creative shapes. Inherited from the ad set on the attach shape. Available goals vary by platform. Meta-specific: `conversions` requires `promotedObject.pixelId` + `promotedObject.customEventType`; `app_promotion` requires `promotedObject.applicationId` + `promotedObject.objectStoreUrl`; `lead_generation` accepts an optional `promotedObject.pageId` (auto-filled from the connected Page when omitted). (enum: engagement, traffic, awareness, video_views, lead_generation, conversions, app_promotion) | [optional]
**budget_amount** | Option<**f64**> | Required on legacy + multi-creative shapes. Inherited on attach. | [optional]
**budget_type** | Option<**BudgetType**> | Required on legacy + multi-creative shapes. Inherited on attach. (enum: daily, lifetime) | [optional]
**currency** | Option<**String**> |  | [optional]
**headline** | Option<**String**> | Required for Meta, Google, and Pinterest on legacy + attach shapes (skip for multi-creative — use `creatives[].headline`). Ignored for TikTok and X/Twitter. Max: Meta=255, Google=30, Pinterest=100. | [optional]
**long_headline** | Option<**String**> | Google Display only. Defaults to `headline` if omitted. | [optional]
**body** | Option<**String**> | Required on legacy + attach shapes. For X/Twitter this is the tweet text (max 280 chars including a ~24-char URL when `linkUrl` is set). Max: Google=90, Pinterest=500. | [optional]
**call_to_action** | Option<**CallToAction**> | Required on legacy + attach shapes for Meta. Honoured on TikTok too — passes through to the Spark Ad creative's `call_to_action`. Ignored by other platforms. Ignored on Meta when `leadGenFormId` is set — lead ads force CTA type to SIGN_UP. (enum: LEARN_MORE, SHOP_NOW, SIGN_UP, BOOK_TRAVEL, CONTACT_US, DOWNLOAD, GET_OFFER, GET_QUOTE, SUBSCRIBE, WATCH_MORE) | [optional]
**lead_gen_form_id** | Option<**String**> | Meta-only. Attaches a Lead Gen (Instant) Form to the creative. Required when `goal=\"lead_generation\"`. Force-overrides the CTA to SIGN_UP. Create a form first via POST /v1/ads/lead-forms. On the multi-creative shape this can also be set per `creatives[i]` to A/B different forms inside one ad set. | [optional]
**link_url** | Option<**String**> | Required on legacy + attach shapes. Skip for multi-creative. | [optional]
**image_url** | Option<**String**> | Image creative for Meta/Google/Pinterest on legacy + attach shapes (mutually exclusive with `video`). Not required for Google Search campaigns. For TikTok, this field carries the VIDEO URL (the TikTok ads endpoint is video-only; the field retains the `imageUrl` name for cross-platform consistency). Ignored for X/Twitter. For Google Display, treated as the landscape image (alias of `images.landscape`); supply `images.square` alongside or the request is rejected. | [optional]
**images** | Option<[**models::CreateStandaloneAdRequestImages**](CreateStandaloneAdRequestImages.md)> |  | [optional]
**video** | Option<[**models::CreateStandaloneAdRequestVideo**](CreateStandaloneAdRequestVideo.md)> |  | [optional]
**creatives** | Option<[**Vec<models::CreateStandaloneAdRequestCreativesInner>**](CreateStandaloneAdRequestCreativesInner.md)> | Meta-only. When present, switches to the multi-creative shape: creates 1 campaign + 1 ad set + N ads (one per entry here). Top-level `headline` / `body` / `imageUrl` / `linkUrl` / `callToAction` are ignored in this mode. Mutually exclusive with `adSetId`.  | [optional]
**ad_set_id** | Option<**String**> | Meta-only. When present, switches to the attach shape: adds one new ad to this existing ad set without creating a new campaign. Budget, targeting, goal, schedule, AND bid strategy are inherited from the ad set on Meta — passing `bidStrategy` in attach mode returns 400. To change an existing ad set's bid, use `PUT /v1/ads/ad-sets/{adSetId}`. Mutually exclusive with `creatives[]`.  Supported on Meta (facebook, instagram) and TikTok. On TikTok the `adSetId` is the ad group ID; the new ad inherits the ad group's bid + budget + targeting.  | [optional]
**business_name** | Option<**String**> | Google Display only | [optional]
**board_id** | Option<**String**> | Pinterest only. Board ID (auto-creates if not provided). | [optional]
**countries** | Option<**Vec<String>**> | ISO 3166-1 alpha-2 country codes (e.g. ['NL']). Defaults to ['US'] when no `cities` or `regions` are provided. | [optional]
**cities** | Option<[**Vec<models::CreateStandaloneAdRequestCitiesInner>**](CreateStandaloneAdRequestCitiesInner.md)> | Meta-only. City-level geo targeting. Each city is targeted by Meta's opaque `key` (the city ID) which can be looked up via `GET /v1/ads/targeting/search?type=city&q=<name>&country_code=<ISO>`. Optional `radius` + `distance_unit` extend the targeting beyond the city limits (e.g. radius 25 km around the city center). Both must be set together, or both omitted (Meta defaults to ~16 km when omitted).  Cannot overlap with the same country in `countries` (Meta returns a \"locations overlap\" error). Either drop the country or scope it to a different country.  | [optional]
**regions** | Option<[**Vec<models::CreateStandaloneAdRequestRegionsInner>**](CreateStandaloneAdRequestRegionsInner.md)> | Meta-only. Region-level (state/province) geo targeting. Each region is targeted by Meta's opaque `key` (the region ID) which can be looked up via `GET /v1/ads/targeting/search?type=region&q=<name>&country_code=<ISO>`.  | [optional]
**age_min** | Option<**i32**> |  | [optional]
**age_max** | Option<**i32**> |  | [optional]
**interests** | Option<[**Vec<models::UpdateAdRequestTargetingInterestsInner>**](UpdateAdRequestTargetingInterestsInner.md)> | Interest objects from /v1/ads/interests. Each must include id and name. | [optional]
**end_date** | Option<**String**> | Required for lifetime budgets | [optional]
**audience_id** | Option<**String**> | Custom audience ID for targeting | [optional]
**campaign_type** | Option<**CampaignType**> | Google only (enum: display, search) | [optional][default to Display]
**keywords** | Option<**Vec<String>**> | Google Search only | [optional]
**additional_headlines** | Option<**Vec<String>**> | Google Search RSA only. Extra headlines. | [optional]
**additional_descriptions** | Option<**Vec<String>**> | Google Search RSA only. Extra descriptions. | [optional]
**advantage_audience** | Option<**AdvantageAudience**> | Meta only. Controls the Advantage audience feature (targeting_automation). 0 = disabled (default), 1 = enabled. Meta Marketing API requires this field on all ad set creation requests. (enum: 0, 1) | [optional]
**gender** | Option<**Gender**> | Meta only. Restrict the audience by gender. 'male' targets men only, 'female' targets women only, 'all' (default) targets everyone. Ignored by non-Meta platforms. (enum: all, male, female) | [optional][default to All]
**bid_strategy** | Option<[**models::BidStrategy**](BidStrategy.md)> | Meta bid strategy applied to the ad set. | [optional]
**bid_amount** | Option<**f64**> | Bid cap in WHOLE currency units (USD: 5 = $5.00; JPY: 100 = ¥100). Required when `bidStrategy` is `LOWEST_COST_WITH_BID_CAP` or `COST_CAP`.  | [optional]
**roas_average_floor** | Option<**f64**> | Minimum ROAS as a decimal multiplier (e.g. 2.0 = 2.0x ROAS). Required when `bidStrategy` is `LOWEST_COST_WITH_MIN_ROAS`. Sent to Meta as `bid_constraints.roas_average_floor` × 10000.  | [optional]
**dsa_beneficiary** | Option<**String**> | Name of the legal entity benefiting from the ad. Required by Meta when targeting EU users (DSA Article 26). Not enforced at schema level; enforced server-side when targeting intersects EU member states.  | [optional]
**dsa_payor** | Option<**String**> | Name of the legal entity paying for the ad. Required by Meta when targeting EU users (DSA Article 26). Note Meta API spelling: dsa_payor (not dsa_payer).  | [optional]
**brand_identity** | Option<[**models::CreateStandaloneAdRequestBrandIdentity**](CreateStandaloneAdRequestBrandIdentity.md)> |  | [optional]
**identity_type** | Option<**IdentityType**> | TikTok only. Forces the identity attribution on the ad:    - `TT_USER`: the posting account's open_id (real @username     branding). Requires a connected TikTok posting account     on the same profile.   - `CUSTOMIZED_USER`: synthetic Brand Identity (display     name + avatar). Requires a configured Brand Identity     (cached on the `tiktokads` SocialAccount via     `PATCH /v1/connect/tiktok-ads`) or an inline     `brandIdentity` to create one on the fly.  When omitted, defaults to `TT_USER` if a posting account is connected on this profile, else `CUSTOMIZED_USER`. Spark Ads (`POST /v1/ads/boost`) always use `TT_USER` regardless of this field — TikTok requires the original organic post's author identity for Spark.  (enum: TT_USER, CUSTOMIZED_USER) | [optional]
**promoted_object** | Option<[**models::CreateStandaloneAdRequestPromotedObject**](CreateStandaloneAdRequestPromotedObject.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


