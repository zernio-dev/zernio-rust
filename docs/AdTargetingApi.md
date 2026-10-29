# \AdTargetingApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**browse_ad_targeting**](AdTargetingApi.md#browse_ad_targeting) | **GET** /v1/ads/targeting/browse | Browse targeting categories
[**estimate_ad_reach**](AdTargetingApi.md#estimate_ad_reach) | **POST** /v1/ads/targeting/reach-estimate | Estimate audience reach
[**get_linked_in_bid_pricing**](AdTargetingApi.md#get_linked_in_bid_pricing) | **POST** /v1/ads/targeting/bid-pricing | Suggested bid and budget bounds
[**get_linked_in_supply_forecast**](AdTargetingApi.md#get_linked_in_supply_forecast) | **POST** /v1/ads/targeting/supply-forecast | Forecast ad delivery
[**search_ad_interests**](AdTargetingApi.md#search_ad_interests) | **GET** /v1/ads/interests | Search targeting interests
[**search_ad_targeting**](AdTargetingApi.md#search_ad_targeting) | **GET** /v1/ads/targeting/search | Search targeting options



## browse_ad_targeting

> models::BrowseAdTargeting200Response browse_ad_targeting(account_id, ad_account_id, r#type, parent_node_id, selectable)
Browse targeting categories

Shows Meta's full tree of detailed targeting categories for an ad account, so you can browse options without a keyword.  It returns the whole Meta detailed-targeting category tree of one ad account (Meta's `GET /act_{ad_account_id}/targetingbrowse`), as one flat list you can render as a tree. Use it to show what can be targeted without a keyword; use `GET /v1/ads/targeting/search` to find an entry by name.  ### Node kinds  Every node is one of two kinds.  **Selectable entity** (`selectable: true`): an interest, behavior or demographic Meta gives an id. `id` plus `type` is what a targeting spec takes.  - `interests`, `behaviors` and `industries` ids go in `TargetingSpec.interests`, `behaviors` and `workIndustries` on `POST /v1/ads/create`. - Every other type goes in `rawTargeting.flexible_spec` under its `type` as the key. - `life_events`, `family_statuses` and `income` take objects (`{ \"flexible_spec\": [{ \"life_events\": [{ \"id\": \"6017476616183\" }] }] }`). - `education_statuses` and `relationship_statuses` take the bare number (`{ \"flexible_spec\": [{ \"education_statuses\": [3] }] }`): Meta answers an object there with a 500.  **Organizational node** (`selectable: false`, `id: null`): a category such as `Demographics > Financial > Income` that only groups other nodes and cannot be targeted.  A few organizational nodes carry a `type` and have no children (`Schools`, `Employers`, `Job titles`, `Fields of study`, `Undergrad years`). Those are open-ended categories Meta only exposes through search (`dimension=workEmployer` / `workPosition` on the search endpoint).  ### Node ids  - `nodeId` identifies a node within this response. - `parentNodeId` points at its parent (`null` for the three roots `Demographics`, `Interests`, `Behaviors`). - A selectable node's `nodeId` is `{type}:{id}`, because Meta reuses small ids across types (education status 3 and relationship status 3 are different entities). - An organizational node's `nodeId` is its full path joined with ` > `.  Labels are kept exactly as Meta sends them, including stray leading or trailing spaces, because Meta has sibling nodes that differ only by whitespace.  The interests branch is Meta's curated browse list (a few hundred entries), not every interest Meta can target: search finds the long tail.  ### No pagination  Meta returns the whole catalog in one response (about 770 nodes) and ignores `limit`, so there is no cursor. Narrow it with `type`, `parentNodeId` and `selectable` instead; they are applied by Zernio.  The catalog is cached for an hour per ad account and connection. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | A connected Meta account (metaads, facebook or instagram). Any other ad platform returns 501 platform_not_supported. | [required] |
**ad_account_id** | **String** | The Meta ad account to browse as, in the form \"act_<digits>\". | [required] |
**r#type** | Option<**String**> | Only the nodes of this Meta type (e.g. interests, behaviors, life_events, income), plus the organizational nodes leading to them. A type that is not in the catalog returns 400. |  |
**parent_node_id** | Option<**String**> | Only the descendants (every depth) of this organizational node, e.g. `Demographics > Financial`. A nodeId that is not an organizational node of the catalog returns 400. |  |
**selectable** | Option<**bool**> | `true` for selectable entities only, `false` for organizational nodes only. |  |

### Return type

[**models::BrowseAdTargeting200Response**](browseAdTargeting_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## estimate_ad_reach

> models::EstimateAdReach200Response estimate_ad_reach(estimate_ad_reach_request)
Estimate audience reach

Estimates how many people a targeting setup would reach before you create a campaign.  Returns a normalized pre-flight audience-size estimate for a targeting spec, before any campaign is created. Backed by each platform's native reach API (Meta `delivery_estimate`, LinkedIn `audienceCounts`, X `audience_summary`, Pinterest `audience_sizing`).  Platforms without a usable pre-flight reach API (Google Search/Display, TikTok) return `available: false` with no bounds, so clients can hide or grey out the estimate rather than treat the absence as an error. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**estimate_ad_reach_request** | [**EstimateAdReachRequest**](EstimateAdReachRequest.md) |  | [required] |

### Return type

[**models::EstimateAdReach200Response**](estimateAdReach_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_linked_in_bid_pricing

> models::GetLinkedInBidPricing200Response get_linked_in_bid_pricing(get_linked_in_bid_pricing_request)
Suggested bid and budget bounds

LinkedIn-only. Returns the suggested bid and bid limits for a targeting spec, plus the daily-budget bounds LinkedIn will accept. Use it before creating a campaign to pick a bid inside the allowed range and warn the user if their daily budget is below the minimum. Wraps LinkedIn's `adBudgetPricing` finder.  Non-LinkedIn accounts return `available: false` so clients can hide the pricing UI without treating it as a failure. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**get_linked_in_bid_pricing_request** | [**GetLinkedInBidPricingRequest**](GetLinkedInBidPricingRequest.md) |  | [required] |

### Return type

[**models::GetLinkedInBidPricing200Response**](getLinkedInBidPricing_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_linked_in_supply_forecast

> models::GetLinkedInSupplyForecast200Response get_linked_in_supply_forecast(get_linked_in_supply_forecast_request)
Forecast ad delivery

LinkedIn-only. Forecasted impressions, clicks, spend and ~20 other metrics for a targeting spec over a time range. Wraps LinkedIn's `adSupplyForecasts` finder.  Each returned series carries a `metricType` (IMPRESSION, CLICK, SPENDING, MAX_POTENTIAL_BUDGET, COST_PER_MILLION_IMPRESSIONS, ...) and a `granularity` (DAILY, SEVEN_DAY, THIRTY_DAY, CUSTOM). LinkedIn caps the daily spending forecast at 1.2x the daily budget and returns 0 once the total budget is exhausted.  Non-LinkedIn accounts return `available: false`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**get_linked_in_supply_forecast_request** | [**GetLinkedInSupplyForecastRequest**](GetLinkedInSupplyForecastRequest.md) |  | [required] |

### Return type

[**models::GetLinkedInSupplyForecast200Response**](getLinkedInSupplyForecast_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## search_ad_interests

> models::SearchAdInterests200Response search_ad_interests(q, account_id)
Search targeting interests

Deprecated alias for `GET /v1/ads/targeting/search?dimension=interest`. Kept for backward compatibility, it returns the legacy `{ interests: [...] }` shape rather than the normalized `{ results: [...] }`. New integrations should use `GET /v1/ads/targeting/search` with `dimension=interest`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** | Search query | [required] |
**account_id** | **String** | Account ID | [required] |

### Return type

[**models::SearchAdInterests200Response**](searchAdInterests_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## search_ad_targeting

> models::SearchAdTargeting200Response search_ad_targeting(account_id, q, dimension, geo_type, country_code, ad_account_id, locale, limit)
Search targeting options

Finds targeting options by name, such as locations, interests or behaviors, and returns the ids to use in ad targeting.  It resolves a human-readable query into the platform's opaque targeting ids used in the `TargetingSpec`: the `countries`/`regions`/`cities`/`zips`/`metros` geo keys and the `interests`/`behaviors` entity ids. Those ids are used on `POST /v1/ads/create`, `POST /v1/ads/targeting/reach-estimate`, and `saved_targeting` audiences.  ### Dimensions  The `dimension` param selects what is searched:  - `geo`: locations, further scoped by `geoType` - `interest` - `interestSuggestion`: Meta only. Interests related to the interest names in `q`, from Meta's interest suggestions (details below) - `behavior`: Meta, TikTok and LinkedIn, matched by name; ids feed `TargetingSpec.behaviors` (details below) - `interestKeyword`: TikTok only. The \"Additional interests\" of TikTok Ads Manager (e.g. `folk` returns `Folk Music`), from TikTok's keyword recommendations for the seed `q` (details below) - `hashtag`: TikTok only. Hashtags recommended for the seed `q`, to target people who viewed videos with them (details below) - `income`: the household-income tiers the platform can target (Meta, TikTok, Google) (details below) - `language`: Google-only - `workPosition`, `workEmployer`, `workIndustry`: the Meta-only work demographics, whose ids feed `TargetingSpec.workPositions`/`workEmployers`/`workIndustries` - `industry`, `jobFunction`, `seniority`, `companySize`, `skill`: the LinkedIn-only B2B facets, whose URNs feed `TargetingSpec.industries`/`jobFunctions`/`seniorities`/`companySizes`/`skills` - `community`: Reddit only. Subreddits matching `q`. The id is the subreddit name for `TargetingSpec.communities` / `excludedCommunities`, `platformId` is Reddit's own id, and `audienceSize` its subscriber count when Reddit reports it - `conversationKeyword`: Reddit only. Reddit's keyword suggestions for the seed `q`. The id is the keyword for `TargetingSpec.conversationKeywords` / `excludedConversationKeywords`  Availability of each dimension varies by platform. A dimension a platform cannot search returns a 400 naming `dimension`. It never falls back to another dimension, and every result's `type` is the requested dimension (or the geo level for `geo`).  Results are normalized across platforms into a single shape, so the same client code consumes Meta, TikTok, LinkedIn, X, Pinterest, Google and Reddit results.  ### `interestSuggestion` (Meta)  `q` lists interest names, case sensitive, names and not ids, in one of two forms:  - Comma-separated: `NBA,Michael Jordan` - For names that contain a comma, a JSON array of strings (`[\"Earth, Wind & Fire\",\"Yoga\"]`, URL-encoded). A `q` starting with `[` is always read as JSON.  A `q` with no name or malformed JSON returns 400 naming `q`.  Meta also suggests behaviors and demographics. Zernio keeps only interests, so every id goes in `TargetingSpec.interests`, like `interest` results. Zernio classifies them with a Meta call pinned to `en_US` (ids whose `path` starts with `Interests`).  Without `locale` results are in English. With another `locale`, a second call in that locale returns the same interests with localized names and `path`.  Zernio asks Meta for three times `limit` (at most 100) before filtering, so fewer than `limit` results can come back. Meta weights the first name heavily: a multi-name `q` mostly returns suggestions for the first one.  ### `behavior`  - Meta: its fixed behaviors catalog (e.g. `Small business owners`, `Frequent Travelers`). - TikTok: video and creator interaction categories (e.g. `Software & Apps`), with ids like `video:1913101` or `creator:24001` and `path` starting with `Video interactions` or `Creator interactions`. Hashtags are their own `hashtag` dimension. - LinkedIn: member behaviors (e.g. `Frequent Travelers`, `Job Seekers`, `Recently Promoted`), ids like `urn:li:memberBehavior:9`. - Google has no separate behavior catalog: its in-market and affinity segments come back from `interest`. - X removed behavior targeting from its Ads API.  ### `interestKeyword` and `hashtag` (TikTok)  - `interestKeyword` ids look like `keyword:123456` and go in `TargetingSpec.interests`, next to interest categories. Only keywords TikTok lets an ad group target come back (`status` `EFFECTIVE`). TikTok returns no audience size. - `hashtag` ids look like `hashtag:123456` and go in `TargetingSpec.behaviors`. Only hashtags TikTok reports `ONLINE` come back. - For `hashtag`, spaces in `q` are removed first, because TikTok recommends no hashtags for a multi-word seed (`acoustic guitar` searches `acousticguitar`).  For both, a `q` made only of prefixed ids (`keyword:101,keyword:102` or `hashtag:201`) looks those ids up instead of searching. Unavailable ones are included with their `status` (`INEFFECTIVE` or `OFFLINE`), so ids read back from an ad group (`interest_keyword_ids`, `actions` in `nativeSettings`) resolve to names.  An `interestKeyword` lookup takes at most 50 ids (more returns 400 naming `q`).  ### `income`  The id is the normalized tier (`top_5`, `top_10`, `top_10_25`, `top_25_50`) to pass as `TargetingSpec.incomeTier`, never a platform segment id.  - Meta: tiers are US-only ZIP-code percentiles (label and `audienceSize` come live from Meta). - TikTok: expresses all four. - Google: only `top_10`.  `q` is matched against the label, so `top` or `income` lists every tier.  ### TikTok `interest`  TikTok `interest` searches TikTok's interest category catalog (about 700 categories over four levels, `path` holds the parent categories), matched by name in Zernio. The ids are what `TargetingSpec.interests` sends to TikTok as `interest_category_ids`.  ### Meta `workIndustry` and Google `language`  Work industries are a fixed ~30-entry Meta catalog with no server-side query, so `workIndustry` matching, ranking and `limit` happen in Zernio.  `language` is likewise a fixed, checked-in table of Google's targetable `language_constant` rows (id, ISO code, name). It is matched by name or code, capped at 20, with no network call. Its ids feed `TargetingSpec.languages`.  ### Geo queries  For geo queries, `q` should contain only the locality name (e.g. `\"Amsterdam\"`, not `\"Amsterdam, NL\"`). Use `countryCode` to disambiguate.  ### TikTok geo  TikTok geo searches return every matching level in one list (`type` is `country`, `region`, `city`, `district`, or `metro` for DMA areas), and `geoType` is not applied.  Results are scoped to the advertiser's targetable markets (pass `adAccountId` when the connection holds several advertisers). A two-letter `q` also matches a country by ISO code (`q=GB` returns the United Kingdom first).  A `country` result's id is its ISO 3166-1 alpha-2 code, for `targeting.countries`. Every other id is TikTok's numeric location id, usable in `regions`/`cities`/`metros` keys on `POST /v1/ads/create`.  ### LinkedIn geo  LinkedIn geo searches also return every matching level in one list. Neither `geoType` nor `countryCode` is applied: LinkedIn's typeahead only returns a name and a URN per result, with no level or country field to filter on.  - A result whose URN is a country Zernio holds a code for has `type: country` and its ISO 3166-1 alpha-2 code as the id, for `targeting.countries`. - Every other result has `type: region` and keeps its `urn:li:geo:*` URN as the id, usable as a `regions[].key` on `POST /v1/ads/create`, `POST /v1/ads/boost` and `POST /v1/ads/targeting/reach-estimate`.  LinkedIn puts countries and regions in the same `locations` facet, so both target the same way.  ### LinkedIn B2B  LinkedIn B2B searches (`industry`, `jobFunction`, `seniority`, `companySize`, `skill`) return the full URN to pass straight back, so no URN id fragment has to be assembled by hand:  - `urn:li:industry:4` - `urn:li:function:8` - `urn:li:seniority:6` - `urn:li:staffCountRange:(51,200)` - `urn:li:skill:1346`  Only `industry` and `skill` are server-side name searches (LinkedIn's typeahead finder).  LinkedIn exposes no typeahead for job functions, seniorities and company sizes. Zernio fetches each whole table (26, 10 and 9 entries), caches it, and does the matching, ranking and `limit` cutoff itself. Those three never carry `audienceSize`.  `countryCode` and `geoType` are not applied to any of the four.  ### Google geo  Google geo searches resolve against Google's geoTargetConstants and return every matching level in one list.  `geoType` is not applied (Google's `target_type` is an open taxonomy that does not map one-to-one onto the `geoType` enum). Filter client-side on the returned `type` (`country`, `region`, `city`, `zip`, `metro`, or the lowercased Google target type for rarer levels). `countryCode` scopes the search to one country.  A `country` result's id is its ISO 3166-1 alpha-2 code, for `targeting.countries`. Every other id is Google's numeric criterion id, usable as a `regions`/`cities`/`zips`/`metros` `key` on `POST /v1/ads/create`.  Google city radius is not supported (pass a `customLocations` lat/lng pin for a radius). Country targeting also accepts plain ISO codes via `countries` with no search call.  ### Pinterest  Pinterest resolves against three whole-catalog endpoints (interests, locations, regions) with no server-side query or pagination. Matching, ranking and the `limit` cutoff all happen in Zernio.  The catalog is independent of any ad account and results never carry `audienceSize`. Names come back localized to the connected Pinterest account's language (there is no way to force a locale), so match against whatever language that account returns.  `geoType` routes to a different Pinterest catalog:  - `country` and `metro_area` read the locations catalog (`type` is `country` or `metro`) - `region` reads the regions catalog (`type` is `region`, its id a `regions[].key` on `POST /v1/ads/create`) - `all` and the default `city` merge both catalogs with honest per-entry `type`s, since Pinterest has no city-level catalog and `city` is an alias for `all`, not a literal city search - `zip`, `subcity`, `neighborhood`, `place` and `geo_market` return a 400: Pinterest exposes no postal-code catalog, pass postal codes directly as `targeting.zips: [{ key }]` on `POST /v1/ads/create`  ### Reddit  Reddit (`redditads` connection) searches `geo`, `interest`, `community` and `conversationKeyword`. Any other dimension returns 400.  Its geo search honours these `geoType` values (other values return 400):  - `city`: the default, a server-side city search - `zip`: `q` is the postal code - `country`, `region` and `metro_area`: matched in Zernio against Reddit's geolocation catalog - `all`  `countryCode` scopes every geo search. Each result's id is Reddit's geolocation id, usable as a `regions`/`metros`/`cities`/`zips` `key` (country ids go in `countries`).  `interest` matches Reddit's interest catalog in Zernio, with the category as `path`.  ### Meta language  Meta matches `q` against names in one language and returns names and `path` in that language. Pass `locale` (e.g. `pl_PL`) to choose it.  Without `locale`:  - The `behavior` and `workIndustry` catalogs and `interestSuggestion` are in `en_US`. - `interest`, `geo`, `workPosition` and `workEmployer` follow the language of the Facebook user who connected the account (so a Russian-language Facebook user gets Russian paths, and Polish names need `locale=pl_PL`).  A non-English `behavior` or `workIndustry` query without `locale` never matches, so pass the locale of the names you search.  Meta's `interest` search matches its own interest names and has no fuzzy or synonym mode. A phrase Meta does not use as an interest name (e.g. `dental implants`) can return nothing while a shorter word (`dentistry`) does.  If Meta returns an empty `behavior`, `workIndustry` or `income` catalog, the request fails with a 502 `platform_api_error` instead of an empty `results` list. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Account ID (a connected account on the target ad platform). | [required] |
**q** | **String** | Search query. For geo, the locality name only (no region/country suffix). For `interestSuggestion`, the interest names: comma-separated, or a JSON array of strings when a name contains a comma (a `q` starting with `[` is read as JSON). | [required] |
**dimension** | Option<**String**> | What to search. Defaults to `interest` for backward compatibility with the deprecated /v1/ads/interests alias.  - `geo`: resolves locations (scope further with `geoType`). - `interest`/`behavior`: resolve audience entities (`behavior` on Meta, TikTok and LinkedIn). - `interestSuggestion`: suggests interests related to the names in `q` (Meta only). - `interestKeyword`/`hashtag`: resolve TikTok additional interests and hashtags (TikTok only). - `income`: resolves the normalized income tiers. - `language`: resolves Google's targetable language_constant table (Google only). - `workPosition`/`workEmployer`/`workIndustry`: resolve Meta work demographics. - `industry`/`jobFunction`/`seniority`/`companySize`/`skill`: resolve LinkedIn B2B facets (LinkedIn only). |  |[default to interest]
**geo_type** | Option<**String**> | Only used when `dimension=geo`. The kind of location to resolve. `all` searches every type in one relevance-ranked call. Defaults to `city`. |  |[default to city]
**country_code** | Option<**String**> | ISO 3166-1 alpha-2 country code (e.g. NL) to scope a geo search. |  |
**ad_account_id** | Option<**String**> | TikTok only: the advertiser to search as, when the connection holds several. Each TikTok advertiser has its own targetable regions and catalogs. Defaults to the connection's first advertiser; an advertiser the connection does not hold returns 400. |  |
**locale** | Option<**String**> | Meta only (ignored on other platforms). The language Meta matches `q` against and names results and `path` in, as language_TERRITORY (e.g. `pl_PL`, `en_US`).  Applies to `geo`, `interest`, `interestSuggestion`, `behavior`, `workPosition`, `workEmployer` and `workIndustry`.  **Without it:** `behavior`, `workIndustry` and `interestSuggestion` use `en_US`; other searches use the language of the Facebook user who connected the account. `income` always uses `en_US`. |  |
**limit** | Option<**i32**> | Maximum results to return. |  |[default to 25]

### Return type

[**models::SearchAdTargeting200Response**](searchAdTargeting_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

