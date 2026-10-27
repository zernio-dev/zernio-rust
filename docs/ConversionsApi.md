# \ConversionsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_conversion_associations**](ConversionsApi.md#add_conversion_associations) | **POST** /v1/accounts/{accountId}/conversion-destinations/{destinationId}/associations | Associate campaigns
[**adjust_conversions**](ConversionsApi.md#adjust_conversions) | **POST** /v1/ads/conversions/adjustments | Adjust uploaded conversions
[**create_conversion_action**](ConversionsApi.md#create_conversion_action) | **POST** /v1/ads/conversions/actions | Create website conversion action
[**create_conversion_destination**](ConversionsApi.md#create_conversion_destination) | **POST** /v1/accounts/{accountId}/conversion-destinations | Create a conversion destination
[**create_custom_conversion_goal**](ConversionsApi.md#create_custom_conversion_goal) | **POST** /v1/ads/conversions/custom-goals | Create a custom conversion goal
[**create_event_destination**](ConversionsApi.md#create_event_destination) | **POST** /v1/events/destinations | Add an event destination
[**delete_conversion_destination**](ConversionsApi.md#delete_conversion_destination) | **DELETE** /v1/accounts/{accountId}/conversion-destinations/{destinationId} | Delete a conversion destination
[**delete_event_destination**](ConversionsApi.md#delete_event_destination) | **DELETE** /v1/events/destinations/{destinationId} | Remove an event destination
[**get_conversion_destination**](ConversionsApi.md#get_conversion_destination) | **GET** /v1/accounts/{accountId}/conversion-destinations/{destinationId} | Get a conversion destination
[**get_conversion_metrics**](ConversionsApi.md#get_conversion_metrics) | **GET** /v1/accounts/{accountId}/conversion-destinations/{destinationId}/metrics | Get attribution metrics
[**get_conversions_quality**](ConversionsApi.md#get_conversions_quality) | **GET** /v1/ads/conversions/quality | Get Event Match Quality
[**list_ad_conversion_goals**](ConversionsApi.md#list_ad_conversion_goals) | **GET** /v1/ads/conversions/goals | List account conversion goals
[**list_conversion_actions**](ConversionsApi.md#list_conversion_actions) | **GET** /v1/ads/conversions/actions | List conversion actions
[**list_conversion_associations**](ConversionsApi.md#list_conversion_associations) | **GET** /v1/accounts/{accountId}/conversion-destinations/{destinationId}/associations | List associated campaigns
[**list_conversion_destinations**](ConversionsApi.md#list_conversion_destinations) | **GET** /v1/accounts/{accountId}/conversion-destinations | List conversion destinations
[**list_custom_conversion_goals**](ConversionsApi.md#list_custom_conversion_goals) | **GET** /v1/ads/conversions/custom-goals | List custom conversion goals
[**list_event_destinations**](ConversionsApi.md#list_event_destinations) | **GET** /v1/events/destinations | List event destinations
[**list_events**](ConversionsApi.md#list_events) | **GET** /v1/events | List stored events
[**remove_conversion_associations**](ConversionsApi.md#remove_conversion_associations) | **DELETE** /v1/accounts/{accountId}/conversion-destinations/{destinationId}/associations | Remove associated campaigns
[**remove_custom_conversion_goal**](ConversionsApi.md#remove_custom_conversion_goal) | **DELETE** /v1/ads/conversions/custom-goals/{goalId} | Remove a custom conversion goal
[**send_conversions**](ConversionsApi.md#send_conversions) | **POST** /v1/ads/conversions | Send conversion events
[**send_events**](ConversionsApi.md#send_events) | **POST** /v1/events | Send events to every destination
[**update_ad_conversion_goals**](ConversionsApi.md#update_ad_conversion_goals) | **PATCH** /v1/ads/conversions/goals | Update account conversion goals
[**update_conversion_action**](ConversionsApi.md#update_conversion_action) | **PATCH** /v1/ads/conversions/actions/{actionId} | Update a conversion action's settings
[**update_conversion_destination**](ConversionsApi.md#update_conversion_destination) | **PATCH** /v1/accounts/{accountId}/conversion-destinations/{destinationId} | Update a conversion destination
[**update_custom_conversion_goal**](ConversionsApi.md#update_custom_conversion_goal) | **PATCH** /v1/ads/conversions/custom-goals/{goalId} | Update a custom conversion goal



## add_conversion_associations

> models::AddConversionAssociations200Response add_conversion_associations(account_id, destination_id, add_conversion_associations_request)
Associate campaigns

Links campaigns to a LinkedIn conversion rule so they track it, reporting which links succeeded or failed.  Returns a per-campaign success/failure result so callers can retry only the rows that failed (e.g. wrong campaign type for the rule's objective). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**destination_id** | **String** |  | [required] |
**add_conversion_associations_request** | [**AddConversionAssociationsRequest**](AddConversionAssociationsRequest.md) |  | [required] |

### Return type

[**models::AddConversionAssociations200Response**](addConversionAssociations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## adjust_conversions

> models::AdjustConversions200Response adjust_conversions(adjust_conversions_request)
Adjust uploaded conversions

Retracts, restates the value of, or enhances conversions you already sent to Google Ads, for refunds or late customer data.  Adjust conversions that were previously uploaded via `POST /v1/ads/conversions`: retract them, restate their value, or enhance them with first-party data. Requires the Ads add-on.  **Google Ads only.** Google handles adjustments through the classic Google Ads API (`ConversionAdjustmentUploadService`); the Data Manager `ingestEvents` path used for sending conversions is ingest-only. Meta and LinkedIn have no equivalent, so this endpoint returns `405` for those platforms.  Adjustment types:  - `RETRACTION`: remove the conversion entirely (refund, chargeback, cancelled order, churn). - `RESTATEMENT`: change the conversion's value (upgrade / downgrade / partial refund). Send the corrected **total** value in `restatementValue` (not a delta). - `ENHANCEMENT`: attach first-party identifiers (hashed email / phone) to an existing conversion (enhanced conversions applied after the fact).  Identifying the original conversion (per adjustment):  - `orderId`: the transaction ID you sent as `eventId` on the original conversion. Recommended, and **required** for `ENHANCEMENT`. - or `gclid` + `conversionTime`: the click ID and the original conversion's time (unix seconds). Not available for `ENHANCEMENT`.  `destinationId` is the conversion action resource name, e.g. `customers/1234567890/conversionActions/987654321` (same value you send to `POST /v1/ads/conversions`). PII in `user` is hashed with SHA-256 server-side (Gmail-specific normalization included). Send plaintext.  Times are unix seconds; we convert to Google's required `yyyy-MM-dd HH:mm:ss+00:00` format. Up to 2000 adjustments per request; partial failure is supported (inspect `adjustmentsFailed` / `failures[]`). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**adjust_conversions_request** | [**AdjustConversionsRequest**](AdjustConversionsRequest.md) |  | [required] |

### Return type

[**models::AdjustConversions200Response**](adjustConversions_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_conversion_action

> models::CreateConversionAction201Response create_conversion_action(create_conversion_action_request)
Create website conversion action

Creates a Google Ads website conversion action and returns the tag snippets to install on your site.  Creates a `WEBPAGE` conversion action (category `DEFAULT`) and returns it with its tag snippets, read back after creation since Google never returns them on the create response itself. Invalidates the cached list `GET` on this resource would otherwise keep serving. Google-only; other platforms return `501`. Requires the Ads add-on. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_conversion_action_request** | [**CreateConversionActionRequest**](CreateConversionActionRequest.md) |  | [required] |

### Return type

[**models::CreateConversionAction201Response**](createConversionAction_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_conversion_destination

> models::CreateConversionDestination201Response create_conversion_destination(account_id, create_conversion_destination_request)
Create a conversion destination

Creates a new place to send conversion events: a Google Ads conversion action or a LinkedIn conversion rule.  Supported for LinkedIn (conversion rule) and Google Ads (conversion action). Meta and OpenAI Ads pixels are created via their own tracking-tags flow instead (`POST /v1/accounts/{accountId}/tracking-tags`); this endpoint returns 405 for both, and for Reddit (create Reddit pixels in Reddit Ads Manager).  **LinkedIn:** creation is NOT idempotent. A retry creates a second destination. Deduplicate before retrying.  **Google Ads:** calling with a name that already exists reuses the existing conversion action transparently (the response is identical to a fresh create). Calling with the same name but a different category returns a typed `IDEMPOTENCY_CONFLICT` (409) rather than silently returning the mismatched action.  **LinkedIn:** the rule is created with `conversionMethod=CONVERSIONS_API` and (by default) auto-associated with all of the ad account's campaigns via `autoAssociationType=ALL_CAMPAIGNS`. Pass `autoAssociationType: NONE` to opt out and manage associations explicitly via the associations endpoints below.  365-day attribution windows are only valid for `SUBMIT_APPLICATION`, `PURCHASE`, `ADD_TO_CART`, `QUALIFIED_LEAD`, and `LEAD` rule types; the API rejects other combinations locally.  **Google Ads:** the conversion action is created with `type=UPLOAD_CLICKS` (required for API-uploaded offline conversions, immutable after creation). The `type` field carries the Google `ConversionActionCategory` enum value, e.g. `PURCHASE`, `SUBSCRIBE_PAID`, `SIGNUP`, `IMPORTED_LEAD`, `BOOK_APPOINTMENT`. Unified standard event names (e.g. `Purchase`, `Subscribe`, `CompleteRegistration`, `Lead`, `Schedule`) are resolved to their Google category equivalents automatically. The action defaults to secondary (non-primary) to avoid immediately steering Smart Bidding; pass `primaryForGoal: true` to opt in. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | SocialAccount ID (linkedinads or googleads). | [required] |
**create_conversion_destination_request** | [**CreateConversionDestinationRequest**](CreateConversionDestinationRequest.md) |  | [required] |

### Return type

[**models::CreateConversionDestination201Response**](createConversionDestination_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_custom_conversion_goal

> models::CreateSharedBudget201ResponseBudget create_custom_conversion_goal(create_custom_conversion_goal_request)
Create a custom conversion goal

Creates a Google Ads custom conversion goal from a set of conversion actions, so a campaign can bid on just those.  Creates a custom conversion goal from conversion action ids. Point a campaign at it with `PATCH /v1/ads/campaigns/{campaignId}/conversion-goals`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_custom_conversion_goal_request** | [**CreateCustomConversionGoalRequest**](CreateCustomConversionGoalRequest.md) |  | [required] |

### Return type

[**models::CreateSharedBudget201ResponseBudget**](createSharedBudget_201_response_budget.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_event_destination

> models::CreateEventDestination201Response create_event_destination(create_event_destination_request)
Add an event destination

Saves an ad platform destination for a profile, so events sent to `POST /v1/events` for that profile are forwarded to it. Pick `destinationId` from `GET /v1/accounts/{accountId}/conversion-destinations`. Set `eventNames` to forward only those events (for example only `Purchase`); leave it out to forward every event. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_event_destination_request** | [**CreateEventDestinationRequest**](CreateEventDestinationRequest.md) |  | [required] |

### Return type

[**models::CreateEventDestination201Response**](createEventDestination_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_conversion_destination

> delete_conversion_destination(account_id, destination_id, ad_account_id)
Delete a conversion destination

Disables a LinkedIn conversion rule, which is how LinkedIn deletes it; the rule can still be read afterwards.  LinkedIn-only today. LinkedIn does not expose hard-delete on conversion rules; what their UI calls \"delete\" is the same `enabled: false` flip we apply here. The rule remains fetchable via GET with `status: 'inactive'`; the unified discovery endpoint hides it by default.  `adAccountId` may be passed as a query parameter (recommended) or as a JSON body field for clients that can send DELETE bodies. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**destination_id** | **String** |  | [required] |
**ad_account_id** | Option<**String**> | Required as query OR in JSON body. |  |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_event_destination

> models::DeleteSmsSenderId200Response delete_event_destination(destination_id)
Remove an event destination

Stops forwarding events to this destination. `destinationId` is the event destination `id`, not the platform destination.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**destination_id** | **String** |  | [required] |

### Return type

[**models::DeleteSmsSenderId200Response**](deleteSmsSenderId_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_conversion_destination

> models::GetConversionDestination200Response get_conversion_destination(account_id, destination_id, ad_account_id)
Get a conversion destination

Shows one LinkedIn conversion rule with its full settings.  LinkedIn-only today. Returns the full destination record for one conversion rule. The `adAccountId` query parameter is required because LinkedIn rules are scoped to a sponsored ad account. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**destination_id** | **String** |  | [required] |
**ad_account_id** | **String** | Numeric ID or full `urn:li:sponsoredAccount:{id}` URN. | [required] |

### Return type

[**models::GetConversionDestination200Response**](getConversionDestination_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_conversion_metrics

> models::GetConversionMetrics200Response get_conversion_metrics(account_id, destination_id, ad_account_id, start_date, end_date, granularity)
Get attribution metrics

Shows a LinkedIn conversion rule's attributed conversions, value, leads and cost over time.  LinkedIn-only today. Returns conversion-attribution metrics (`externalWebsiteConversions`, `externalWebsitePostClickConversions`, `externalWebsitePostViewConversions`, `conversionValueInLocalCurrency`, `qualifiedLeads`, `costInLocalCurrency`) bucketed by date.  Date-range constraints (passed through from LinkedIn): - `granularity=DAILY` is retained for ~6 months only - `granularity=ALL` with a range > 6 months auto-rounds to month boundaries - `granularity=MONTHLY`/`YEARLY` retains 24 months  Throttle: LinkedIn caps adAnalytics at 45M metric values per 5-minute window across the calling token. Single-rule queries are well within that limit; surfaces as 429 if hit. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**destination_id** | **String** |  | [required] |
**ad_account_id** | **String** |  | [required] |
**start_date** | **String** |  | [required] |
**end_date** | Option<**String**> |  |  |
**granularity** | Option<**String**> |  |  |[default to DAILY]

### Return type

[**models::GetConversionMetrics200Response**](getConversionMetrics_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_conversions_quality

> models::GetConversionsQuality200Response get_conversions_quality(account_id, destination_id)
Get Event Match Quality

Shows how well your server-side conversion events match users, with event match quality and coverage for Meta or Pinterest.  Reads Meta Event Match Quality (EMQ) and pixel↔CAPI event coverage for a pixel/dataset, live from Meta's Dataset Quality API. Web events only (a Meta limitation). Other platforms return 405, except Pinterest. Requires the Ads add-on.  Pinterest (`pinterestads`): `destinationId` is the numeric ad account id. Rows come from Pinterest's Event Quality Score for Conversions API web events over the last 14 days, one per event name, with each identifier's coverage in `matchKeys` and `eventCoveragePercentage` set to the tag/API `event_id` overlap. No `compositeScore`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | SocialAccount _id (a metaads or pinterestads account). | [required] |
**destination_id** | **String** | Meta pixel/dataset ID, or the numeric Pinterest ad account id. | [required] |

### Return type

[**models::GetConversionsQuality200Response**](getConversionsQuality_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ad_conversion_goals

> models::ListAdConversionGoals200Response list_ad_conversion_goals(account_id, ad_account_id, customer_id)
List account conversion goals

Lists a Google Ads account's default conversion goals, which ones are used for bidding, and the conversion actions in each.  Google Ads account-default conversion goals (CustomerConversionGoal), one per category and origin, with `biddable` (whether the goal is used for bidding and reported in the Conversions column) and the conversion actions that belong to it, each flagged `primaryForGoal` (primary) or not (secondary). Reads are cached for 10 minutes; when the shared Google quota is exhausted the last successful result is served with `stale: true`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id (Google Ads) | [required] |
**ad_account_id** | Option<**String**> | Google customer id. Required when the connection has multiple customers. |  |
**customer_id** | Option<**String**> | Alias of adAccountId |  |

### Return type

[**models::ListAdConversionGoals200Response**](listAdConversionGoals_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_conversion_actions

> models::ListConversionActions200Response list_conversion_actions(account_id, ad_account_id, customer_id, r#type)
List conversion actions

Lists the conversion actions in a Google Ads account, with the website tag snippets to install where available.  Lists Google Ads conversion actions on the resolved customer, all types by default. Each action's `tagSnippets` (global site tag + event snippet) is included when Google has them for that action's type, e.g. `WEBPAGE`. Google-only; other platforms return `501`. Requires the Ads add-on.  `adAccountId` (alias `customerId`) is optional: when omitted, it is resolved from the connection's accessible Google Ads customers, and the call fails with `400` when more than one is accessible (pass `adAccountId` to disambiguate).  The list itself is cached for the quota window (1 hour fresh, up to 7 days last-good; the cache key does not vary on `type`). The response carries `cachedAt` and `stale`, set when a quota-exhausted call falls back to the last-good copy instead of a live read. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | SocialAccount _id (must be a googleads account). | [required] |
**ad_account_id** | Option<**String**> | Platform ad account ID (Google customer ID, digits only). Resolved automatically when the connection has exactly one accessible customer. |  |
**customer_id** | Option<**String**> | Alias of adAccountId, kept for existing callers |  |
**r#type** | Option<**String**> | Filter by Google's ConversionActionType enum (e.g. WEBPAGE, UPLOAD_CLICKS). |  |

### Return type

[**models::ListConversionActions200Response**](listConversionActions_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_conversion_associations

> models::ListConversionAssociations200Response list_conversion_associations(account_id, destination_id, ad_account_id)
List associated campaigns

Lists the LinkedIn campaigns that track a conversion rule, so you can spot newer campaigns that still need linking.  LinkedIn-only today. Returns the campaigns currently associated with this conversion rule. Auto-association on rule creation runs once at create time; campaigns created after the rule still need explicit association. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**destination_id** | **String** |  | [required] |
**ad_account_id** | **String** |  | [required] |

### Return type

[**models::ListConversionAssociations200Response**](listConversionAssociations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_conversion_destinations

> models::ListConversionDestinations200Response list_conversion_destinations(account_id)
List conversion destinations

Lists where an ad account can receive conversion events (pixels, conversion actions or rules), so you know where to send them.  Returns the list of pixels (Meta), conversion actions (Google), conversion rules (LinkedIn), pixels (OpenAI Ads, Reddit) or ad accounts (Pinterest) accessible to the connected ads account. Use the returned `id` as `destinationId` when posting to `POST /v1/ads/conversions`.  For Google and LinkedIn, each destination's `type` reflects the conversion type (PURCHASE, LEAD, SIGN_UP, etc.), and the event type is locked to the destination. For Meta, OpenAI Ads and Reddit, `type` is absent: pixels accept any event name per request.  For Reddit, the pixels of every ad account the connection reaches (only the scoped ones when the connection has an ad-account scope), each with the `adAccountId` that owns it. Reddit pixels are created in Reddit Ads Manager, not through Zernio.  For LinkedIn, destinations are returned across every sponsored ad account the connected token can access; the `adAccountId` field on each destination identifies the parent ad account and is required for subsequent CRUD calls (update, delete, associations, metrics). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | SocialAccount ID (metaads, googleads, linkedinads, tiktokads, openaiads, pinterestads, or redditads). | [required] |

### Return type

[**models::ListConversionDestinations200Response**](listConversionDestinations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_custom_conversion_goals

> models::ListCustomConversionGoals200Response list_custom_conversion_goals(account_id, ad_account_id, customer_id)
List custom conversion goals

Lists the custom conversion goals in a Google Ads account, each a named set of conversion actions a campaign can bid on.  Google Ads custom conversion goals (a named set of conversion actions a campaign can bid on). Removed goals are excluded. Cached like the other Google reads. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id (Google Ads) | [required] |
**ad_account_id** | Option<**String**> | Google customer id. Required when the connection has multiple customers. |  |
**customer_id** | Option<**String**> | Alias of adAccountId |  |

### Return type

[**models::ListCustomConversionGoals200Response**](listCustomConversionGoals_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_event_destinations

> models::ListEventDestinations200Response list_event_destinations(profile_id)
List event destinations

Lists the ad platform destinations that receive events sent to `POST /v1/events`, for one profile or every profile you can access.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | Option<**String**> |  |  |

### Return type

[**models::ListEventDestinations200Response**](listEventDestinations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_events

> models::ListEvents200Response list_events(profile_id, limit, from, to, event_name, cursor)
List stored events

Lists the conversion events stored for a profile by `POST /v1/events`, newest first. Personal data is never returned: `hasEmail`, `hasPhone` and `hasExternalId` only say whether the event carried that identifier. Events sent with `testCode` are not stored, so they never appear here.  Paginate with `cursor`: pass the `nextCursor` of the previous page until it comes back `null`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | **String** |  | [required] |
**limit** | Option<**i32**> |  |  |[default to 50]
**from** | Option<**String**> | Only events at or after this time (ISO 8601, on the event time). |  |
**to** | Option<**String**> | Only events before this time (ISO 8601, on the event time). |  |
**event_name** | Option<**String**> | Only events with this name, such as `Purchase`. |  |
**cursor** | Option<**String**> | `nextCursor` from the previous page. |  |

### Return type

[**models::ListEvents200Response**](listEvents_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_conversion_associations

> models::RemoveConversionAssociations200Response remove_conversion_associations(account_id, destination_id, ad_account_id, campaign_ids)
Remove associated campaigns

Unlinks campaigns from a LinkedIn conversion rule so they stop tracking it.  Pass `adAccountId` and `campaignIds` as query parameters (`campaignIds` is comma-separated). The route also accepts a JSON body with the same fields for clients that prefer DELETE-with-body, but the documented surface is query-only because some SDK code generators (e.g. Python) collapse query + body parameters with the same name into a single kwarg. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**destination_id** | **String** |  | [required] |
**ad_account_id** | **String** |  | [required] |
**campaign_ids** | **String** | Comma-separated list of campaign IDs. | [required] |

### Return type

[**models::RemoveConversionAssociations200Response**](removeConversionAssociations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_custom_conversion_goal

> models::RemoveCustomConversionGoal200Response remove_custom_conversion_goal(goal_id, account_id, ad_account_id, customer_id)
Remove a custom conversion goal

Deletes a Google Ads custom conversion goal; switch any campaigns using it to another goal first.  Google refuses (400) while any campaign still uses it: switch those campaigns to another goal first. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**goal_id** | **String** | Google custom conversion goal id | [required] |
**account_id** | **String** | Zernio SocialAccount id (Google Ads) | [required] |
**ad_account_id** | Option<**String**> | Google customer id. Required when the connection has multiple customers. |  |
**customer_id** | Option<**String**> | Alias of adAccountId |  |

### Return type

[**models::RemoveCustomConversionGoal200Response**](removeCustomConversionGoal_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## send_conversions

> models::SendConversions200Response send_conversions(send_conversions_request)
Send conversion events

Sends conversion events, such as purchases or leads, from your server to an ad platform so it can attribute and optimize ads.  Relay one or more conversion events to the target ad platform's native Conversions API. Platform is inferred from the provided `accountId`. Requires the Ads add-on.  Supported platforms:  - Meta (`metaads`) via Graph API - Google Ads (`googleads`) via Data Manager API `ingestEvents` - LinkedIn (`linkedinads`) via `/rest/conversionEvents` - TikTok (`tiktokads`) via the Offline Events API `/offline/batch/` (OFFLINE conversions only) - OpenAI Ads (`openaiads`) via its Conversions API (a separate host, `bzr.openai.com`) - Pinterest (`pinterestads`) via `POST /v5/ad_accounts/{id}/events` - Reddit (`redditads`) via the Reddit Conversions API (`POST /api/v3/pixels/{pixelId}/conversion_events`)  `destinationId` semantics differ per platform:  - Meta: pixel (dataset) ID, e.g. `123456789012345` - Google: conversion action resource name, e.g. `customers/1234567890/conversionActions/987654321` - LinkedIn: conversion rule ID or URN, e.g. `104012` or `urn:lla:llaPartnerConversion:104012` - TikTok: Offline Event Set ID, e.g. `7057103914977558530` - OpenAI Ads: pixel wire id (numeric `pixel_id`, distinct from the internal pixel id), as returned by `GET /v1/accounts/{accountId}/conversion-destinations` - Pinterest: numeric ad account id, e.g. `549755885175` (Pinterest attributes to the ad account, not to a tag) - Reddit: pixel id, e.g. `a2_abc123`, as returned by `GET /v1/accounts/{accountId}/conversion-destinations` (any other shape returns 400)  Pinterest notes: each event needs an `email`, or `ipAddress` plus `userAgent`; others are listed in `failures` with code `INVALID_EVENT` and the rest are still sent. `clickIds.epik` (the `_epik` cookie) is sent as `click_id`. `actionSource` `web` stays `web`, offline sources become `offline`, and app events need `platformData.action_source` `app_android` or `app_ios`. Pinterest answers per event, so one bad event does not fail its chunk (failures carry code `PINTEREST_EVENT_FAILED`). `consent.adUserData: DENIED` sets `opt_out`. The connected user needs a Business Access role on the ad account (403 otherwise).  Reddit notes: each event needs a match key: `clickIds.rdt_cid`, `clickIds.rdt_uuid`, `email`, `phone`, `externalId`, or `ipAddress` plus `userAgent`. Reddit accepts events up to 7 days old, and `eventTime` is unix SECONDS (a value more than an hour in the future is refused as milliseconds). Events failing these checks are listed in `failures` with code `INVALID_EVENT` and the rest are still sent. Email (lowercased, dots and `+tags` stripped from the local part), phone (E.164 with the leading `+`) and `externalId` are SHA-256 hashed; IP and user agent go plaintext. `consent.adUserData: DENIED` sends no user fields. `actionSource` maps to WEBSITE (`web`), APP (`app`) or OTHER, overridable with `platformData.action_source`; `platformData.order_id` is forwarded. `testCode` is sent as Reddit's `test_id`. The connection must hold the `adsconversions` permission: one authorized without it returns 403 `reconnect_required` (reconnect via GET /v1/connect/redditads/ads), and a Reddit user with no role on the ad account that owns the pixel returns 403 `insufficient_permissions`. Reddit throttling and other rejections are reported per chunk in `failures` with code `REDDIT_REJECTED`.  TikTok notes: this path sends OFFLINE conversions (in-store / CRM / call-center), not web-pixel events. Each event must carry an email or phone (TikTok requires at least one). The connected TikTok ads account must have granted the Offline Events permission; older grants must reconnect.  OpenAI Ads notes: requires a tracking tag (pixel) to already exist on the account. Returns 422 with code `TRACKING_TAG_REQUIRED` if `POST /v1/accounts/{accountId}/tracking-tags` hasn't been called yet.  Callers can list valid destinations via `GET /v1/accounts/{accountId}/conversion-destinations`.  All PII (email, phone, names, external IDs) is hashed with SHA-256 server-side per each platform's normalization spec, including Google's Gmail-specific dot/plus-suffix stripping. Send plaintext. LinkedIn `externalIds` are passed through as plaintext per LinkedIn's spec; only emails and phones are hashed.  For LinkedIn, the connected account must have been authorized after the Conversions API rollout (i.e. the OAuth grant must include `rw_conversions`). Older accounts must reconnect.  Batching is handled automatically. Meta caps at 1000 events per request and rejects the entire batch if any event is malformed. Google caps at 2000. LinkedIn caps at 5000 and is also all-or-nothing per chunk. OpenAI Ads caps at 1000 per request; larger submissions are split into 1000-event chunks, each all-or-nothing (a malformed event fails every event in that chunk, not the whole request). Reddit works the same way, in chunks of 1000.  Dedup: pass a stable `eventId` on every event. Meta and LinkedIn use it to dedupe against browser-side pixel/Insight Tag events; Google maps it to `transactionId`; Reddit receives it as `conversion_id`, its dedup key against Reddit Pixel events.  Per-platform `eventName` semantics:  - Meta: free-form. Standard names (Purchase, Lead, ...) match Meta's built-in events; custom strings are accepted. - Google: ignored. The conversion action's category determines the event type. Send the standard name closest to your action for documentation, but the platform will not branch on it. - LinkedIn: ignored. The conversion rule's `type` (LEAD, PURCHASE, etc.) is locked to the destination at rule-creation time. Send the standard name for documentation; LinkedIn does not branch on it. - OpenAI Ads: a fixed subset of standard names (Purchase, Lead, AddToCart, ViewContent, InitiateCheckout, CompleteRegistration, Subscribe, StartTrial, Schedule) maps 1:1 onto OpenAI's own event-type enum; any other standard name or custom string is sent as `type: custom` with the name preserved. - Pinterest: standard names map onto Pinterest's (Purchase = `checkout`, AddToCart = `add_to_cart`, InitiateCheckout = `initiate_checkout`, AddPaymentInfo = `add_payment_info`, Lead = `lead`, CompleteRegistration = `signup`, Subscribe = `subscribe`, ViewContent = `view_content`, Search = `search`, PageView = `page_visit`); any other string is sent as is, so it matches an advertiser defined event of that name. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**send_conversions_request** | [**SendConversionsRequest**](SendConversionsRequest.md) |  | [required] |

### Return type

[**models::SendConversions200Response**](sendConversions_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## send_events

> models::SendEvents200Response send_events(send_events_request)
Send events to every destination

Sends conversion events once and forwards them to every ad platform destination saved for the profile (see `POST /v1/events/destinations`), or to the `destinations` given in the request. Each destination receives the events exactly as `POST /v1/ads/conversions` would send them, so the per-platform notes there (hashing, batching, `eventName` semantics, dedup on `eventId`) apply here too. A destination saved with `eventNames` only receives events with those names.  Zernio also stores each event for the profile's reporting. Email, phone and `externalId` are stored only as SHA-256 hashes, and `sourceUrl` keeps only its origin, path and attribution parameters (`utm_*`, `gclid`, `fbclid`, `ttclid`, `li_fat_id`, `epik`, `rdt_cid`, `gbraid`, `wbraid`). Events sent with `testCode` are forwarded but not stored.  One destination failing never blocks the others: each one reports its own result. Requires the Ads add-on. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**send_events_request** | [**SendEventsRequest**](SendEventsRequest.md) |  | [required] |

### Return type

[**models::SendEvents200Response**](sendEvents_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_ad_conversion_goals

> models::UpdateAdConversionGoals200Response update_ad_conversion_goals(update_ad_conversion_goals_request)
Update account conversion goals

Turns bidding on or off for a Google Ads account's default conversion goals, which campaigns using account goals follow.  Sets `biddable` on one or more account-default goals, addressed by category and origin, in one mutate. Campaigns that use account-level goals (`goalConfigLevel: CUSTOMER`) follow the change. Returns the re-read goal list.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**update_ad_conversion_goals_request** | [**UpdateAdConversionGoalsRequest**](UpdateAdConversionGoalsRequest.md) |  | [required] |

### Return type

[**models::UpdateAdConversionGoals200Response**](updateAdConversionGoals_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_conversion_action

> models::UpdateConversionAction200Response update_conversion_action(action_id, update_conversion_action_request)
Update a conversion action's settings

Changes a Google Ads conversion action's settings, such as primary or secondary, counting, value and lookback windows, or removes or restores it.  Updates a Google Ads conversion action in one mutate, each field sent written on its own update mask leaf so omitted fields keep their value. Send at least one field.  `primaryForGoal` sets `primary_for_goal`: a primary action counts toward its goal's bidding and the Conversions column; a secondary one is observation-only (All conversions). `countingType`, `category`, the value settings (`defaultValue`, `defaultCurrency`, `alwaysUseDefaultValue`) and the click-through / view-through lookback windows map to the same-named conversion_action fields.  `status: REMOVED` removes the action (Google keeps it, with its history, as REMOVED) and must be sent alone; `status: ENABLED` restores a removed action. Google refuses HIDDEN on website actions, so it is not offered.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**action_id** | **String** | Google conversion action id | [required] |
**update_conversion_action_request** | [**UpdateConversionActionRequest**](UpdateConversionActionRequest.md) |  | [required] |

### Return type

[**models::UpdateConversionAction200Response**](updateConversionAction_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_conversion_destination

> models::GetConversionDestination200Response update_conversion_destination(account_id, destination_id, update_conversion_destination_request)
Update a conversion destination

Changes a LinkedIn conversion rule's name, value, attribution windows, or turns it on or off.  Partial-update a conversion rule. LinkedIn-only today. Whitelisted fields: `name`, `enabled`, attribution windows, `valueType`, `value`, `attributionType`. The rule's `type` and parent ad account are intentionally not exposed for update. Recreate the rule if those need to change. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**destination_id** | **String** |  | [required] |
**update_conversion_destination_request** | [**UpdateConversionDestinationRequest**](UpdateConversionDestinationRequest.md) |  | [required] |

### Return type

[**models::GetConversionDestination200Response**](getConversionDestination_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_custom_conversion_goal

> models::UpdateCustomConversionGoal200Response update_custom_conversion_goal(goal_id, update_custom_conversion_goal_request)
Update a custom conversion goal

Renames a Google Ads custom conversion goal or replaces the conversion actions in it.  Returns the re-read goal. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**goal_id** | **String** | Google custom conversion goal id | [required] |
**update_custom_conversion_goal_request** | [**UpdateCustomConversionGoalRequest**](UpdateCustomConversionGoalRequest.md) |  | [required] |

### Return type

[**models::UpdateCustomConversionGoal200Response**](updateCustomConversionGoal_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

