# CreateCtwaAdRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Facebook or Instagram SocialAccount ID. | 
**ad_account_id** | **String** | Meta ad account ID, e.g. `act_123456789`. | 
**name** | **String** | Ad display name. Used to derive campaign / ad set names. On the multi-creative shape, each ad's Meta name gets a \" #N\" suffix (1-indexed) so Ads Manager shows them as a numbered batch.  | 
**headline** | Option<**String**> | Single-creative shape only. Mutually exclusive with `creatives[]`.  | [optional]
**body** | Option<**String**> | Primary text shown above the image / video. Single-creative shape only. Mutually exclusive with `creatives[]`.  | [optional]
**image_url** | Option<**String**> | Image asset for single-creative shape. Mutually exclusive with `video` and with `creatives[]`. Required on the single-creative shape if `video` is not supplied.  | [optional]
**video** | Option<[**models::CreateCtwaAdRequestVideo**](CreateCtwaAdRequestVideo.md)> |  | [optional]
**creatives** | Option<[**Vec<models::CreateCtwaAdRequestCreativesInner>**](CreateCtwaAdRequestCreativesInner.md)> | Multi-creative shape: N CTWA ads under one campaign + one ad set, sharing budget and targeting. Mutually exclusive with the top-level single-creative fields (`headline` / `body` / `imageUrl` / `video`). Each entry must supply its own headline, body, and exactly one of `imageUrl` / `video`.  | [optional]
**budget_amount** | **f64** | Budget amount in the ad account's currency major units (e.g. dollars for USD, not cents). Must be > 0.  | 
**budget_type** | **BudgetType** |  (enum: daily, lifetime) | 
**currency** | Option<**String**> | ISO 4217 currency code matching the ad account's currency (e.g. `USD`). Optional; Meta infers from the ad account when omitted.  | [optional]
**end_date** | Option<**String**> | ISO 8601 datetime. Required when `budgetType` is `lifetime`.  | [optional]
**countries** | Option<**Vec<String>**> | ISO 3166-1 alpha-2 country codes. Defaults to `[\"US\"]` only when no other geo (`cities`, `regions`, `zips`, `metros`, `customLocations`) is supplied.  | [optional]
**cities** | Option<[**Vec<models::CreateCtwaAdRequestCitiesInner>**](CreateCtwaAdRequestCitiesInner.md)> | City-level geo targeting for local CTWA campaigns (e.g. 25km radius around Milan). Each entry maps to Meta's TargetingGeoLocationCity. `key` is Meta's city ID (lookupable via GET /v1/ads/targeting/search). `radius` and `distance_unit` are coupled: set both or neither.  | [optional]
**regions** | Option<[**Vec<models::CreateCtwaAdRequestRegionsInner>**](CreateCtwaAdRequestRegionsInner.md)> | Region / state-level geo targeting. `key` is Meta's region ID (lookupable via GET /v1/ads/targeting/search?type=region).  | [optional]
**zips** | Option<[**Vec<models::CreateCtwaAdRequestZipsInner>**](CreateCtwaAdRequestZipsInner.md)> | ZIP / postal-code geo targeting. `key` is the platform's postal id resolved via /v1/ads/targeting/search.  | [optional]
**metros** | Option<[**Vec<models::CreateCtwaAdRequestZipsInner>**](CreateCtwaAdRequestZipsInner.md)> | DMA / metro-area geo targeting. `key` is Meta's metro id (e.g. `DMA:807`).  | [optional]
**custom_locations** | Option<[**Vec<models::CreateStandaloneAdRequestCustomLocationsInner>**](CreateStandaloneAdRequestCustomLocationsInner.md)> | Point-radius geo (Meta `geo_locations.custom_locations`). Use for targeting a radius around a specific lat/long when no Meta city/region key fits. `distanceUnit` is required.  | [optional]
**age_min** | Option<**i32**> |  | [optional]
**age_max** | Option<**i32**> |  | [optional]
**interests** | Option<[**Vec<models::CreateStandaloneAdRequestBehaviorsInner>**](CreateStandaloneAdRequestBehaviorsInner.md)> |  | [optional]
**audience_id** | Option<**String**> | Custom audience ID to target. | [optional]
**placements** | Option<[**models::CreateCtwaAdRequestPlacements**](CreateCtwaAdRequestPlacements.md)> |  | [optional]
**advantage_audience** | Option<**AdvantageAudience**> | Meta's Advantage+ audience expansion. `0` (default) keeps targeting strict; `1` lets Meta expand beyond the supplied targeting when its delivery system finds better matches. Always sent on CREATE (Meta requires it).  (enum: 0, 1) | [optional]
**objective** | Option<**Objective**> | Defaults to `OUTCOME_ENGAGEMENT` (the broadly-supported CTWA objective). `OUTCOME_SALES` and `OUTCOME_LEADS` require additional account configuration (Dataset linked to the WABA for sales) and may be rejected by Meta if missing.  (enum: OUTCOME_ENGAGEMENT, OUTCOME_SALES, OUTCOME_LEADS) | [optional]
**bid_strategy** | Option<**BidStrategy**> | Meta bid strategy applied to the shared ad set. Defaults to `LOWEST_COST_WITHOUT_CAP` (auto-bid) when omitted. `LOWEST_COST_WITH_BID_CAP` and `COST_CAP` require `bidAmount`. `LOWEST_COST_WITH_MIN_ROAS` requires `roasAverageFloor`. CTWA's `optimization_goal` is fixed to `CONVERSATIONS`, but the bid strategy is independent.  (enum: LOWEST_COST_WITHOUT_CAP, LOWEST_COST_WITH_BID_CAP, COST_CAP, LOWEST_COST_WITH_MIN_ROAS) | [optional]
**bid_amount** | Option<**f64**> | Whole currency units (e.g. `5` = $5.00 on a USD account). Required when `bidStrategy` is `LOWEST_COST_WITH_BID_CAP` or `COST_CAP`; rejected otherwise.  | [optional]
**roas_average_floor** | Option<**f64**> | Decimal ROAS multiplier (e.g. `2.0` = 2.0× ROAS floor). Required when `bidStrategy` is `LOWEST_COST_WITH_MIN_ROAS`; rejected otherwise. Meta enforces its own upper bound server-side.  | [optional]
**dsa_beneficiary** | Option<**String**> | Legal entity that benefits from the ad. Required when targeting EU users (EU DSA, Article 26). Optional if the ad account has a default beneficiary: set it once via `PATCH /v1/ads/accounts` or in Meta Ads Manager, and Meta fills it in whenever the field is omitted.  | [optional]
**dsa_payor** | Option<**String**> | Legal entity that pays for the ad. Can differ from `dsaBeneficiary` (for example, an agency paying for a client's ads). Same rules as `dsaBeneficiary`: required for EU targeting unless the ad account has a default payor.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


