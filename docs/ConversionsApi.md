# \ConversionsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_ad_conversion_associations**](ConversionsApi.md#add_ad_conversion_associations) | **POST** /v1/ads/conversions/destinations/{destinationId}/associations | Associate campaigns
[**add_conversion_associations**](ConversionsApi.md#add_conversion_associations) | **POST** /v1/accounts/{accountId}/conversion-destinations/{destinationId}/associations | Associate campaigns
[**adjust_conversions**](ConversionsApi.md#adjust_conversions) | **POST** /v1/ads/conversions/adjustments | Adjust uploaded conversions
[**create_ad_conversion_destination**](ConversionsApi.md#create_ad_conversion_destination) | **POST** /v1/ads/conversions/destinations | Create a conversion destination
[**create_ad_custom_conversion**](ConversionsApi.md#create_ad_custom_conversion) | **POST** /v1/ads/conversions/custom-conversions | Create custom conversion
[**create_conversion_action**](ConversionsApi.md#create_conversion_action) | **POST** /v1/ads/conversions/actions | Create conversion action
[**create_conversion_destination**](ConversionsApi.md#create_conversion_destination) | **POST** /v1/accounts/{accountId}/conversion-destinations | Create a conversion destination
[**create_custom_conversion_goal**](ConversionsApi.md#create_custom_conversion_goal) | **POST** /v1/ads/conversions/custom-goals | Create a custom conversion goal
[**create_event_destination**](ConversionsApi.md#create_event_destination) | **POST** /v1/events/destinations | Add an event destination
[**create_forwarding_rule**](ConversionsApi.md#create_forwarding_rule) | **POST** /v1/events/forwarding-rules | Add a forwarding rule
[**delete_ad_conversion_destination**](ConversionsApi.md#delete_ad_conversion_destination) | **DELETE** /v1/ads/conversions/destinations/{destinationId} | Delete a conversion destination
[**delete_conversion_destination**](ConversionsApi.md#delete_conversion_destination) | **DELETE** /v1/accounts/{accountId}/conversion-destinations/{destinationId} | Delete a conversion destination
[**delete_event_destination**](ConversionsApi.md#delete_event_destination) | **DELETE** /v1/events/destinations/{destinationId} | Remove an event destination
[**delete_forwarding_rule**](ConversionsApi.md#delete_forwarding_rule) | **DELETE** /v1/events/forwarding-rules/{ruleId} | Remove a forwarding rule
[**get_ad_conversion_destination**](ConversionsApi.md#get_ad_conversion_destination) | **GET** /v1/ads/conversions/destinations/{destinationId} | Get a conversion destination
[**get_ad_conversion_metrics**](ConversionsApi.md#get_ad_conversion_metrics) | **GET** /v1/ads/conversions/destinations/{destinationId}/metrics | Get attribution metrics
[**get_conversion_destination**](ConversionsApi.md#get_conversion_destination) | **GET** /v1/accounts/{accountId}/conversion-destinations/{destinationId} | Get a conversion destination
[**get_conversion_metrics**](ConversionsApi.md#get_conversion_metrics) | **GET** /v1/accounts/{accountId}/conversion-destinations/{destinationId}/metrics | Get attribution metrics
[**get_conversions_quality**](ConversionsApi.md#get_conversions_quality) | **GET** /v1/ads/conversions/quality | Get Event Match Quality
[**get_event**](ConversionsApi.md#get_event) | **GET** /v1/events/{eventId} | Get one stored event and its deliveries
[**get_events_overview**](ConversionsApi.md#get_events_overview) | **GET** /v1/events/overview | Get today's tracking overview
[**list_ad_conversion_associations**](ConversionsApi.md#list_ad_conversion_associations) | **GET** /v1/ads/conversions/destinations/{destinationId}/associations | List associated campaigns
[**list_ad_conversion_destinations**](ConversionsApi.md#list_ad_conversion_destinations) | **GET** /v1/ads/conversions/destinations | List conversion destinations
[**list_ad_conversion_goals**](ConversionsApi.md#list_ad_conversion_goals) | **GET** /v1/ads/conversions/goals | List account conversion goals
[**list_ad_custom_conversions**](ConversionsApi.md#list_ad_custom_conversions) | **GET** /v1/ads/conversions/custom-conversions | List custom conversions
[**list_conversion_actions**](ConversionsApi.md#list_conversion_actions) | **GET** /v1/ads/conversions/actions | List conversion actions
[**list_conversion_associations**](ConversionsApi.md#list_conversion_associations) | **GET** /v1/accounts/{accountId}/conversion-destinations/{destinationId}/associations | List associated campaigns
[**list_conversion_destinations**](ConversionsApi.md#list_conversion_destinations) | **GET** /v1/accounts/{accountId}/conversion-destinations | List conversion destinations
[**list_custom_conversion_goals**](ConversionsApi.md#list_custom_conversion_goals) | **GET** /v1/ads/conversions/custom-goals | List custom conversion goals
[**list_event_destinations**](ConversionsApi.md#list_event_destinations) | **GET** /v1/events/destinations | List event destinations
[**list_events**](ConversionsApi.md#list_events) | **GET** /v1/events | List stored events
[**list_forwarding_rules**](ConversionsApi.md#list_forwarding_rules) | **GET** /v1/events/forwarding-rules | List forwarding rules
[**remove_ad_conversion_associations**](ConversionsApi.md#remove_ad_conversion_associations) | **DELETE** /v1/ads/conversions/destinations/{destinationId}/associations | Remove associated campaigns
[**remove_conversion_associations**](ConversionsApi.md#remove_conversion_associations) | **DELETE** /v1/accounts/{accountId}/conversion-destinations/{destinationId}/associations | Remove associated campaigns
[**remove_custom_conversion_goal**](ConversionsApi.md#remove_custom_conversion_goal) | **DELETE** /v1/ads/conversions/custom-goals/{goalId} | Remove a custom conversion goal
[**restate_event**](ConversionsApi.md#restate_event) | **PATCH** /v1/events/{eventId} | Change a stored event's value
[**retract_event**](ConversionsApi.md#retract_event) | **DELETE** /v1/events/{eventId} | Retract a stored event
[**send_conversions**](ConversionsApi.md#send_conversions) | **POST** /v1/ads/conversions | Send conversion events
[**send_events**](ConversionsApi.md#send_events) | **POST** /v1/events | Send events to every destination
[**update_ad_conversion_destination**](ConversionsApi.md#update_ad_conversion_destination) | **PATCH** /v1/ads/conversions/destinations/{destinationId} | Update a conversion destination
[**update_ad_conversion_goals**](ConversionsApi.md#update_ad_conversion_goals) | **PATCH** /v1/ads/conversions/goals | Update account conversion goals
[**update_conversion_action**](ConversionsApi.md#update_conversion_action) | **PATCH** /v1/ads/conversions/actions/{actionId} | Update a conversion action's settings
[**update_conversion_destination**](ConversionsApi.md#update_conversion_destination) | **PATCH** /v1/accounts/{accountId}/conversion-destinations/{destinationId} | Update a conversion destination
[**update_custom_conversion_goal**](ConversionsApi.md#update_custom_conversion_goal) | **PATCH** /v1/ads/conversions/custom-goals/{goalId} | Update a custom conversion goal
[**update_forwarding_rule**](ConversionsApi.md#update_forwarding_rule) | **PATCH** /v1/events/forwarding-rules/{ruleId} | Change a forwarding rule's API secret



## add_ad_conversion_associations

> models::AddAdConversionAssociations200Response add_ad_conversion_associations(destination_id, add_ad_conversion_associations_request)
Associate campaigns

Links campaigns to a LinkedIn conversion rule so they track it, reporting which links succeeded or failed.  Returns a per-campaign success/failure result so callers can retry only the rows that failed (e.g. wrong campaign type for the rule's objective). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**destination_id** | **String** |  | [required] |
**add_ad_conversion_associations_request** | [**AddAdConversionAssociationsRequest**](AddAdConversionAssociationsRequest.md) |  | [required] |

### Return type

[**models::AddAdConversionAssociations200Response**](addAdConversionAssociations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## add_conversion_associations

> models::AddAdConversionAssociations200Response add_conversion_associations(account_id, destination_id, add_conversion_associations_request)
Associate campaigns

The first path of `POST /v1/ads/conversions/destinations/{destinationId}/associations` (`addAdConversionAssociations`), which does the same with `accountId` as a parameter. It keeps working. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**destination_id** | **String** |  | [required] |
**add_conversion_associations_request** | [**AddConversionAssociationsRequest**](AddConversionAssociationsRequest.md) |  | [required] |

### Return type

[**models::AddAdConversionAssociations200Response**](addAdConversionAssociations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## adjust_conversions

> models::AdjustConversions200Response adjust_conversions(adjust_conversions_request)
Adjust uploaded conversions

Retracts, restates the value of, or enhances conversions you already sent to Google Ads, for refunds or late customer data. To change Zernio's stored event too, and every platform at once, use `PATCH` or `DELETE /v1/events/{eventId}`.  It adjusts conversions previously uploaded via `POST /v1/ads/conversions`: retract them, restate their value, or enhance them with first-party data. Requires the Ads add-on.  ### Google Ads only  Google handles adjustments through the classic Google Ads API (`ConversionAdjustmentUploadService`). The Data Manager `ingestEvents` path used for sending conversions is ingest-only. Meta and LinkedIn have no equivalent, so this endpoint returns `405` for those platforms.  ### Adjustment types  - `RETRACTION`: remove the conversion entirely (refund, chargeback, cancelled order, churn). - `RESTATEMENT`: change the conversion's value (upgrade / downgrade / partial refund). Send the corrected **total** value in `restatementValue` (not a delta). - `ENHANCEMENT`: attach first-party identifiers (hashed email / phone) to an existing conversion (enhanced conversions applied after the fact).  ### Identifying the original conversion  Per adjustment, send one of:  - `orderId`: the transaction ID you sent as `eventId` on the original conversion. Recommended, and **required** for `ENHANCEMENT`. - `gclid` + `conversionTime`: the click ID and the original conversion's time (unix seconds). Not available for `ENHANCEMENT`.  ### Other fields  - `destinationId` is the conversion action resource name, e.g. `customers/1234567890/conversionActions/987654321` (same value you send to `POST /v1/ads/conversions`). - PII in `user` is hashed with SHA-256 server-side (Gmail-specific normalization included). Send plaintext. - Times are unix seconds; we convert to Google's required `yyyy-MM-dd HH:mm:ss+00:00` format.  ### Limits  Up to 2000 adjustments per request. Partial failure is supported (inspect `adjustmentsFailed` / `failures[]`). 

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


## create_ad_conversion_destination

> models::CreateAdConversionDestination201Response create_ad_conversion_destination(create_ad_conversion_destination_request)
Create a conversion destination

Creates a new place to send conversion events: a Google Ads conversion action or a LinkedIn conversion rule.  Supported for LinkedIn (conversion rule) and Google Ads (conversion action). It returns 405 for:  - Meta and OpenAI Ads: their pixels are created via their own tracking-tags flow instead (`POST /v1/accounts/{accountId}/tracking-tags`) - Reddit: create Reddit pixels in Reddit Ads Manager  ### LinkedIn  Creation is NOT idempotent. A retry creates a second destination. Deduplicate before retrying.  The rule is created with `conversionMethod=CONVERSIONS_API` and (by default) auto-associated with all of the ad account's campaigns via `autoAssociationType=ALL_CAMPAIGNS`. Pass `autoAssociationType: NONE` to opt out and manage associations explicitly via the associations endpoints below.  365-day attribution windows are only valid for these rule types; the API rejects other combinations locally:  - `SUBMIT_APPLICATION` - `PURCHASE` - `ADD_TO_CART` - `QUALIFIED_LEAD` - `LEAD`  ### Google Ads  Calling with a name that already exists reuses the existing conversion action transparently (the response is identical to a fresh create).  Calling with the same name but a different category, or a name already used by a website (`WEBPAGE`) action, returns a typed `IDEMPOTENCY_CONFLICT` (409) rather than silently returning the mismatched action.  The conversion action is created with `type=UPLOAD_CLICKS` (required for API-uploaded offline conversions, immutable after creation).  The `type` field carries the Google `ConversionActionCategory` enum value, e.g. `PURCHASE`, `SUBSCRIBE_PAID`, `SIGNUP`, `IMPORTED_LEAD`, `BOOK_APPOINTMENT`. Unified standard event names (e.g. `Purchase`, `Subscribe`, `CompleteRegistration`, `Lead`, `Schedule`) are resolved to their Google category equivalents automatically.  The action defaults to secondary (non-primary) to avoid immediately steering Smart Bidding; pass `primaryForGoal: true` to opt in. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_ad_conversion_destination_request** | [**CreateAdConversionDestinationRequest**](CreateAdConversionDestinationRequest.md) |  | [required] |

### Return type

[**models::CreateAdConversionDestination201Response**](createAdConversionDestination_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_ad_custom_conversion

> models::CustomConversionResult create_ad_custom_conversion(create_ad_custom_conversion_request)
Create custom conversion

Creates a Meta custom conversion for ads to optimise toward, reusing an existing one with the same name and pixel.  It provisions the Meta custom conversion an ads flow optimises toward, and hands back the `customConversionId` for `promotedObject.customConversionId` on POST /v1/ads/create. This removes the manual \"create it in Ads Manager first\" step.  ### Reuse is ours, not Meta's  Meta's create is not idempotent, so a retried request would otherwise mint a duplicate carrying none of the original's optimisation history.  A non-archived conversion with the same `name` on the same `pixelId` is returned instead of created, with `reused: true` and a 200 rather than a 201.  ### Rule  `rule` is forwarded verbatim in Meta's own grammar (e.g. `{\"url\": {\"i_contains\": \"thank-you\"}}`). Meta validates it and rejects a malformed one with \"A conversion rule is required at creation time\". 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_ad_custom_conversion_request** | [**CreateAdCustomConversionRequest**](CreateAdCustomConversionRequest.md) |  | [required] |

### Return type

[**models::CustomConversionResult**](CustomConversionResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_conversion_action

> models::CreateConversionAction201Response create_conversion_action(create_conversion_action_request)
Create conversion action

Creates a Google Ads conversion action: a website one counted by a tag on your site, or one counted from the conversions you send to Zernio.  - `type: WEBPAGE` creates a website action and returns it with the tag snippets to install, read back after creation since Google never returns them on the create response itself. - `type: UPLOAD_CLICKS` creates an action for the conversions sent with `POST /v1/events`, the same action `POST /v1/ads/conversions/destinations` creates. It is secondary unless `primaryForGoal: true`.  The category defaults to `DEFAULT`. A name already used by another action returns Google's error.  Clears the cached list that `GET` on this resource would otherwise keep serving. Google-only; other platforms return `501`. Requires the Ads add-on. 

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

> models::CreateAdConversionDestination201Response create_conversion_destination(account_id, create_conversion_destination_request)
Create a conversion destination

The first path of `POST /v1/ads/conversions/destinations` (`createAdConversionDestination`), which does the same with `accountId` as a parameter. It keeps working. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | SocialAccount ID (linkedinads or googleads). | [required] |
**create_conversion_destination_request** | [**CreateConversionDestinationRequest**](CreateConversionDestinationRequest.md) |  | [required] |

### Return type

[**models::CreateAdConversionDestination201Response**](createAdConversionDestination_201_response.md)

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

The first name of `POST /v1/events/forwarding-rules`, which saves the same rule. It keeps working and answers under `destination`.

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


## create_forwarding_rule

> models::CreateForwardingRule201Response create_forwarding_rule(create_forwarding_rule_request)
Add a forwarding rule

Saves where a profile's events go: every event sent to `POST /v1/events` for that profile is then forwarded to this destination.  Pick `destinationId` from `GET /v1/ads/conversions/destinations`. Set `eventNames` to forward only those events, such as only `Purchase`; leave it out to forward every event. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_forwarding_rule_request** | [**CreateForwardingRuleRequest**](CreateForwardingRuleRequest.md) |  | [required] |

### Return type

[**models::CreateForwardingRule201Response**](createForwardingRule_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_ad_conversion_destination

> delete_ad_conversion_destination(account_id, destination_id, ad_account_id)
Delete a conversion destination

Disables a LinkedIn conversion rule, which is how LinkedIn deletes it; the rule can still be read afterwards.  LinkedIn-only today. LinkedIn does not expose hard-delete on conversion rules; what their UI calls \"delete\" is the same `enabled: false` flip we apply here. The rule remains fetchable via GET with `status: 'inactive'`; the unified discovery endpoint hides it by default.  `adAccountId` may be passed as a query parameter (recommended) or as a JSON body field for clients that can send DELETE bodies. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The connected ads account (SocialAccount ID). | [required] |
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


## delete_conversion_destination

> delete_conversion_destination(account_id, destination_id, ad_account_id)
Delete a conversion destination

The first path of `DELETE /v1/ads/conversions/destinations/{destinationId}` (`deleteAdConversionDestination`), which does the same with `accountId` as a parameter. It keeps working. 

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

The first name of `DELETE /v1/events/forwarding-rules/{ruleId}`. `destinationId` here is the rule `id`, not the platform destination.

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


## delete_forwarding_rule

> models::DeleteSmsSenderId200Response delete_forwarding_rule(rule_id)
Remove a forwarding rule

Stops forwarding events to this rule's destination. Events already sent are not affected.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**rule_id** | **String** | The rule `id`. | [required] |

### Return type

[**models::DeleteSmsSenderId200Response**](deleteSmsSenderId_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad_conversion_destination

> models::GetAdConversionDestination200Response get_ad_conversion_destination(account_id, destination_id, ad_account_id)
Get a conversion destination

Shows one LinkedIn conversion rule with its full settings.  LinkedIn-only today. Returns the full destination record for one conversion rule. The `adAccountId` query parameter is required because LinkedIn rules are scoped to a sponsored ad account. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The connected ads account (SocialAccount ID). | [required] |
**destination_id** | **String** |  | [required] |
**ad_account_id** | **String** | Numeric ID or full `urn:li:sponsoredAccount:{id}` URN. | [required] |

### Return type

[**models::GetAdConversionDestination200Response**](getAdConversionDestination_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad_conversion_metrics

> models::GetAdConversionMetrics200Response get_ad_conversion_metrics(account_id, destination_id, ad_account_id, start_date, end_date, granularity)
Get attribution metrics

Shows a LinkedIn conversion rule's attributed conversions, value, leads and cost over time.  LinkedIn-only today. Returns conversion-attribution metrics (`externalWebsiteConversions`, `externalWebsitePostClickConversions`, `externalWebsitePostViewConversions`, `conversionValueInLocalCurrency`, `qualifiedLeads`, `costInLocalCurrency`) bucketed by date.  Date-range constraints (passed through from LinkedIn): - `granularity=DAILY` is retained for ~6 months only - `granularity=ALL` with a range > 6 months auto-rounds to month boundaries - `granularity=MONTHLY`/`YEARLY` retains 24 months  Throttle: LinkedIn caps adAnalytics at 45M metric values per 5-minute window across the calling token. Single-rule queries are well within that limit; surfaces as 429 if hit. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The connected ads account (SocialAccount ID). | [required] |
**destination_id** | **String** |  | [required] |
**ad_account_id** | **String** |  | [required] |
**start_date** | **String** |  | [required] |
**end_date** | Option<**String**> |  |  |
**granularity** | Option<**String**> |  |  |[default to DAILY]

### Return type

[**models::GetAdConversionMetrics200Response**](getAdConversionMetrics_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_conversion_destination

> models::GetAdConversionDestination200Response get_conversion_destination(account_id, destination_id, ad_account_id)
Get a conversion destination

The first path of `GET /v1/ads/conversions/destinations/{destinationId}` (`getAdConversionDestination`), which does the same with `accountId` as a parameter. It keeps working. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**destination_id** | **String** |  | [required] |
**ad_account_id** | **String** | Numeric ID or full `urn:li:sponsoredAccount:{id}` URN. | [required] |

### Return type

[**models::GetAdConversionDestination200Response**](getAdConversionDestination_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_conversion_metrics

> models::GetAdConversionMetrics200Response get_conversion_metrics(account_id, destination_id, ad_account_id, start_date, end_date, granularity)
Get attribution metrics

The first path of `GET /v1/ads/conversions/destinations/{destinationId}/metrics` (`getAdConversionMetrics`), which does the same with `accountId` as a parameter. It keeps working. 

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

[**models::GetAdConversionMetrics200Response**](getAdConversionMetrics_200_response.md)

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


## get_event

> models::GetEvent200Response get_event(event_id, profile_id)
Get one stored event and its deliveries

Returns one stored event of a profile (the latest copy of it) and, for each destination it was forwarded to, the newest send: `sent`, `retrying` (failed for now and queued again) or `failed` (final). Requires the Ads add-on. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**event_id** | **String** | The `eventId` the event was sent with. | [required] |
**profile_id** | **String** | Profile the event belongs to. | [required] |

### Return type

[**models::GetEvent200Response**](getEvent_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_events_overview

> models::GetEventsOverview200Response get_events_overview(profile_id)
Get today's tracking overview

How a profile's conversion tracking is doing today (UTC day): events stored, how many reached the ad platforms, each forwarding rule's destination, each event source and, when the profile has a tracking site, the site's funnel. Requires the Ads add-on. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | **String** |  | [required] |

### Return type

[**models::GetEventsOverview200Response**](getEventsOverview_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ad_conversion_associations

> models::ListAdConversionAssociations200Response list_ad_conversion_associations(account_id, destination_id, ad_account_id)
List associated campaigns

Lists the LinkedIn campaigns that track a conversion rule, so you can spot newer campaigns that still need linking.  LinkedIn-only today. Returns the campaigns currently associated with this conversion rule. Auto-association on rule creation runs once at create time; campaigns created after the rule still need explicit association. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The connected ads account (SocialAccount ID). | [required] |
**destination_id** | **String** |  | [required] |
**ad_account_id** | **String** |  | [required] |

### Return type

[**models::ListAdConversionAssociations200Response**](listAdConversionAssociations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ad_conversion_destinations

> models::ListAdConversionDestinations200Response list_ad_conversion_destinations(account_id)
List conversion destinations

Lists where an ad account can receive conversion events (pixels, conversion actions or rules), so you know where to send them.  Returns the list of pixels (Meta), conversion actions (Google), conversion rules (LinkedIn), pixels (OpenAI Ads, Reddit) or ad accounts (Pinterest) accessible to the connected ads account. Use the returned `id` as `destinationId` when posting to `POST /v1/ads/conversions`.  For Google and LinkedIn, each destination's `type` reflects the conversion type (PURCHASE, LEAD, SIGN_UP, etc.), and the event type is locked to the destination. For Meta, OpenAI Ads and Reddit, `type` is absent: pixels accept any event name per request.  For Reddit, the pixels of every ad account the connection reaches (only the scoped ones when the connection has an ad-account scope), each with the `adAccountId` that owns it. Reddit pixels are created in Reddit Ads Manager, not through Zernio.  For LinkedIn, destinations are returned across every sponsored ad account the connected token can access; the `adAccountId` field on each destination identifies the parent ad account and is required for subsequent CRUD calls (update, delete, associations, metrics). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | SocialAccount ID (metaads, googleads, linkedinads, tiktokads, openaiads, pinterestads, or redditads). | [required] |

### Return type

[**models::ListAdConversionDestinations200Response**](listAdConversionDestinations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ad_conversion_goals

> models::ListAdConversionGoals200Response list_ad_conversion_goals(account_id, ad_account_id, customer_id)
List account conversion goals

Lists a Google Ads account's default conversion goals, which ones are used for bidding, and the conversion actions in each.  These are Google Ads account-default conversion goals (CustomerConversionGoal), one per category and origin. Each goal carries:  - `biddable`: whether the goal is used for bidding and reported in the Conversions column. - The conversion actions that belong to it, each flagged `primaryForGoal` (primary) or not (secondary).  ### Caching  Reads are cached for 10 minutes. When the shared Google quota is exhausted, the last successful result is served with `stale: true`. 

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


## list_ad_custom_conversions

> models::ListAdCustomConversions200Response list_ad_custom_conversions(account_id, ad_account_id)
List custom conversions

Lists a Meta ad account's custom conversions, including archived ones.  The ad account's Meta custom conversions, including archived ones (`isArchived`). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Meta ads SocialAccount id. | [required] |
**ad_account_id** | **String** | Meta ad account id (act_<n>). | [required] |

### Return type

[**models::ListAdCustomConversions200Response**](listAdCustomConversions_200_response.md)

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

> models::ListAdConversionAssociations200Response list_conversion_associations(account_id, destination_id, ad_account_id)
List associated campaigns

The first path of `GET /v1/ads/conversions/destinations/{destinationId}/associations` (`listAdConversionAssociations`), which does the same with `accountId` as a parameter. It keeps working. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**destination_id** | **String** |  | [required] |
**ad_account_id** | **String** |  | [required] |

### Return type

[**models::ListAdConversionAssociations200Response**](listAdConversionAssociations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_conversion_destinations

> models::ListAdConversionDestinations200Response list_conversion_destinations(account_id)
List conversion destinations

The first path of `GET /v1/ads/conversions/destinations` (`listAdConversionDestinations`), which does the same with `accountId` as a parameter. It keeps working. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | SocialAccount ID (metaads, googleads, linkedinads, tiktokads, openaiads, pinterestads, or redditads). | [required] |

### Return type

[**models::ListAdConversionDestinations200Response**](listAdConversionDestinations_200_response.md)

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

The first name of `GET /v1/events/forwarding-rules`, which lists the same rules. It keeps working and answers under `destinations`.

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

> models::ListEvents200Response list_events(profile_id, limit, from, to, event_name, source, platform, delivery_status, cursor)
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
**source** | Option<**String**> | Only events from this source, such as `stripe` for the payments of a connected Stripe account. |  |
**platform** | Option<**String**> | Only events sent to this ad platform, such as `metaads` or `googleads`. |  |
**delivery_status** | Option<**String**> | Only events whose latest send to a destination (of `platform`, when given) was accepted (`sent`) or was not (`failed`: failed or still retrying). |  |
**cursor** | Option<**String**> | `nextCursor` from the previous page. |  |

### Return type

[**models::ListEvents200Response**](listEvents_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_forwarding_rules

> models::ListForwardingRules200Response list_forwarding_rules(profile_id)
List forwarding rules

Lists the forwarding rules of one profile, or of every profile you can access. A rule sends a profile's events to one ad platform destination.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | Option<**String**> |  |  |

### Return type

[**models::ListForwardingRules200Response**](listForwardingRules_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_ad_conversion_associations

> models::RemoveAdConversionAssociations200Response remove_ad_conversion_associations(account_id, destination_id, ad_account_id, campaign_ids)
Remove associated campaigns

Unlinks campaigns from a LinkedIn conversion rule so they stop tracking it.  Pass `adAccountId` and `campaignIds` as query parameters (`campaignIds` is comma-separated).  The route also accepts a JSON body with the same fields, for clients that prefer DELETE-with-body. The documented surface is query-only because some SDK code generators (e.g. Python) collapse query + body parameters with the same name into a single kwarg. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The connected ads account (SocialAccount ID). | [required] |
**destination_id** | **String** |  | [required] |
**ad_account_id** | **String** |  | [required] |
**campaign_ids** | **String** | Comma-separated list of campaign IDs. | [required] |

### Return type

[**models::RemoveAdConversionAssociations200Response**](removeAdConversionAssociations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_conversion_associations

> models::RemoveAdConversionAssociations200Response remove_conversion_associations(account_id, destination_id, ad_account_id, campaign_ids)
Remove associated campaigns

The first path of `DELETE /v1/ads/conversions/destinations/{destinationId}/associations` (`removeAdConversionAssociations`), which does the same with `accountId` as a parameter. It keeps working. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**destination_id** | **String** |  | [required] |
**ad_account_id** | **String** |  | [required] |
**campaign_ids** | **String** | Comma-separated list of campaign IDs. | [required] |

### Return type

[**models::RemoveAdConversionAssociations200Response**](removeAdConversionAssociations_200_response.md)

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


## restate_event

> models::RestateEvent200Response restate_event(event_id, restate_event_request)
Change a stored event's value

Changes the value of an event you already sent, for a partial refund or an upgrade. Send the corrected total, not a difference.  Zernio stores a new version of the event, so campaign results count the new value at once. It then passes the change to each destination the event reached: Google Ads restates the conversion, and platforms without a correction API report `not_supported` and keep their count. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**event_id** | **String** | The `eventId` the event was sent with. | [required] |
**restate_event_request** | [**RestateEventRequest**](RestateEventRequest.md) |  | [required] |

### Return type

[**models::RestateEvent200Response**](restateEvent_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## retract_event

> models::RetractEvent200Response retract_event(event_id, profile_id)
Retract a stored event

Retracts an event you already sent, for a refund, a cancelled order or a lost deal. It stops counting in campaign results and ad rules.  Each destination the event reached is told where the platform allows it: Google Ads retracts the conversion, and the other platforms report `not_supported` and keep their count. Sending the same `eventId` again stores it anew. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**event_id** | **String** | The `eventId` the event was sent with. | [required] |
**profile_id** | **String** | Profile the event belongs to. | [required] |

### Return type

[**models::RetractEvent200Response**](retractEvent_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## send_conversions

> models::SendConversions200Response send_conversions(send_conversions_request)
Send conversion events

Sends conversion events, such as purchases or leads, from your server to an ad platform so it can attribute and optimize ads.  Relays one or more events to the target ad platform's native Conversions API. The platform is inferred from the provided `accountId`. Requires the Ads add-on.  ### Supported platforms  - Meta (`metaads`) via Graph API - Google Ads (`googleads`) via Data Manager API `ingestEvents` - LinkedIn (`linkedinads`) via `/rest/conversionEvents` - TikTok (`tiktokads`) via the Offline Events API `/offline/batch/` (OFFLINE conversions only) - OpenAI Ads (`openaiads`) via its Conversions API (a separate host, `bzr.openai.com`) - Pinterest (`pinterestads`) via `POST /v5/ad_accounts/{id}/events` - Reddit (`redditads`) via the Reddit Conversions API (`POST /api/v3/pixels/{pixelId}/conversion_events`)  ### `destinationId` per platform  - Meta: pixel (dataset) ID, e.g. `123456789012345` - Google: conversion action resource name, e.g. `customers/1234567890/conversionActions/987654321` - LinkedIn: conversion rule ID or URN, e.g. `104012` or `urn:lla:llaPartnerConversion:104012` - TikTok: Offline Event Set ID, e.g. `7057103914977558530` - OpenAI Ads: pixel wire id (numeric `pixel_id`, distinct from the internal pixel id), as returned by `GET /v1/ads/conversions/destinations` - Pinterest: numeric ad account id, e.g. `549755885175` (Pinterest attributes to the ad account, not to a tag) - Reddit: pixel id, e.g. `a2_abc123`, as returned by `GET /v1/ads/conversions/destinations` (any other shape returns 400)  Callers can list valid destinations via `GET /v1/ads/conversions/destinations`.  ### Pinterest notes  - Each event needs an `email`, or `ipAddress` plus `userAgent`. Others are listed in `failures` with code `INVALID_EVENT` and the rest are still sent. - `clickIds.epik` (the `_epik` cookie) is sent as `click_id`. - `actionSource` `web` stays `web`, offline sources become `offline`, and app events need `platformData.action_source` `app_android` or `app_ios`. - Pinterest answers per event, so one bad event does not fail its chunk (failures carry code `PINTEREST_EVENT_FAILED`). - `consent.adUserData: DENIED` sets `opt_out`. - The connected user needs a Business Access role on the ad account (403 otherwise).  ### Reddit notes  - Each event needs a match key: `clickIds.rdt_cid`, `clickIds.rdt_uuid`, `email`, `phone`, `externalId`, or `ipAddress` plus `userAgent`. - Reddit accepts events up to 7 days old. `eventTime` is unix SECONDS (a value more than an hour in the future is refused as milliseconds). - Events failing these checks are listed in `failures` with code `INVALID_EVENT` and the rest are still sent. - Email (lowercased, dots and `+tags` stripped from the local part), phone (E.164 with the leading `+`) and `externalId` are SHA-256 hashed. IP and user agent go plaintext. - `consent.adUserData: DENIED` sends no user fields. - `actionSource` maps to WEBSITE (`web`), APP (`app`) or OTHER, overridable with `platformData.action_source`. `platformData.order_id` is forwarded. - `testCode` is sent as Reddit's `test_id`.  Reddit errors:  - 403 `reconnect_required`: the connection was authorized without the `adsconversions` permission (reconnect via GET /v1/connect/redditads/ads). - 403 `insufficient_permissions`: the Reddit user has no role on the ad account that owns the pixel. - `REDDIT_REJECTED`: Reddit throttling and other rejections, reported per chunk in `failures`.  ### TikTok notes  This path sends OFFLINE conversions (in-store / CRM / call-center), not web-pixel events. Each event must carry an email or phone (TikTok requires at least one).  The connected TikTok ads account must have granted the Offline Events permission; older grants must reconnect.  ### OpenAI Ads notes  Requires a tracking tag (pixel) to already exist on the account. Returns 422 with code `TRACKING_TAG_REQUIRED` if `POST /v1/accounts/{accountId}/tracking-tags` hasn't been called yet.  ### Hashing  All PII (email, phone, names, external IDs) is hashed with SHA-256 server-side per each platform's normalization spec, including Google's Gmail-specific dot/plus-suffix stripping. Send plaintext.  LinkedIn `externalIds` are passed through as plaintext per LinkedIn's spec; only emails and phones are hashed.  For LinkedIn, the connected account must have been authorized after the Conversions API rollout (the OAuth grant must include `rw_conversions`). Older accounts must reconnect.  ### Batching  Batching is handled automatically. Per-platform caps:  - Meta: 1000 events per request; rejects the entire batch if any event is malformed. - Google: 2000. - LinkedIn: 5000, all-or-nothing per chunk. - OpenAI Ads: 1000 per request. Larger submissions are split into 1000-event chunks, each all-or-nothing (a malformed event fails every event in that chunk, not the whole request). - Reddit: works the same way as OpenAI Ads, in chunks of 1000.  ### Dedup  Pass a stable `eventId` on every event:  - Meta and LinkedIn use it to dedupe against browser-side pixel/Insight Tag events. - Google maps it to `transactionId`. - Reddit receives it as `conversion_id`, its dedup key against Reddit Pixel events.  ### `eventName` per platform  - Meta: free-form. Standard names (Purchase, Lead, ...) match Meta's built-in events; custom strings are accepted. - Google: ignored. The conversion action's category determines the event type. Send the standard name closest to your action for documentation, but the platform will not branch on it. - LinkedIn: ignored. The conversion rule's `type` (LEAD, PURCHASE, etc.) is locked to the destination at rule-creation time. Send the standard name for documentation; LinkedIn does not branch on it. - OpenAI Ads: a fixed subset of standard names maps 1:1 onto OpenAI's own event-type enum: Purchase, Lead, AddToCart, ViewContent, InitiateCheckout, CompleteRegistration, Subscribe, StartTrial, Schedule. Any other standard name or custom string is sent as `type: custom` with the name preserved. - Pinterest: standard names map onto Pinterest's (see below). Any other string is sent as is, so it matches an advertiser defined event of that name.  Pinterest name mapping:  - Purchase = `checkout` - AddToCart = `add_to_cart` - InitiateCheckout = `initiate_checkout` - AddPaymentInfo = `add_payment_info` - Lead = `lead` - CompleteRegistration = `signup` - Subscribe = `subscribe` - ViewContent = `view_content` - Search = `search` - PageView = `page_visit` 

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

> models::SendEvents200Response send_events(send_events_request, idempotency_key)
Send events to every destination

Sends conversion events once and forwards them to every ad platform destination saved for the profile (see `POST /v1/events/destinations`), or to the `destinations` given in the request. Requires the Ads add-on.  ### Forwarding  - Each destination receives the events exactly as `POST /v1/ads/conversions` would send them, so the per-platform notes there (hashing, batching, `eventName` semantics, dedup on `eventId`) apply here too. - A destination saved with `eventNames` only receives events with those names. - One destination failing never blocks the others: each one reports its own result.  ### Storage  Zernio also stores each event for the profile's reporting.  - Email, phone and `externalId` are stored only as SHA-256 hashes. - `sourceUrl` keeps only its origin, path and attribution parameters (`utm_*`, `gclid`, `fbclid`, `ttclid`, `li_fat_id`, `epik`, `rdt_cid`, `gbraid`, `wbraid`). - Events sent with `testCode` are forwarded but not stored. - Sending an event again with the same `eventId` replaces the stored one. - A stored `Purchase`, `Lead` or `QualifiedLead` tied to one of your campaigns (see `campaign` on each event) counts in `GET /v1/ads/campaign-results` and in ad rules as `sales` and `revenue`, `leads` or `qualified_leads`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**send_events_request** | [**SendEventsRequest**](SendEventsRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  |  |

### Return type

[**models::SendEvents200Response**](sendEvents_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_ad_conversion_destination

> models::GetAdConversionDestination200Response update_ad_conversion_destination(destination_id, update_ad_conversion_destination_request)
Update a conversion destination

Changes a LinkedIn conversion rule's name, value, attribution windows, or turns it on or off.  Partial-update a conversion rule. LinkedIn-only today. Whitelisted fields: `name`, `enabled`, attribution windows, `valueType`, `value`, `attributionType`. The rule's `type` and parent ad account are intentionally not exposed for update. Recreate the rule if those need to change. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**destination_id** | **String** |  | [required] |
**update_ad_conversion_destination_request** | [**UpdateAdConversionDestinationRequest**](UpdateAdConversionDestinationRequest.md) |  | [required] |

### Return type

[**models::GetAdConversionDestination200Response**](getAdConversionDestination_200_response.md)

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

> models::GetAdConversionDestination200Response update_conversion_destination(account_id, destination_id, update_conversion_destination_request)
Update a conversion destination

The first path of `PATCH /v1/ads/conversions/destinations/{destinationId}` (`updateAdConversionDestination`), which does the same with `accountId` as a parameter. It keeps working. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**destination_id** | **String** |  | [required] |
**update_conversion_destination_request** | [**UpdateConversionDestinationRequest**](UpdateConversionDestinationRequest.md) |  | [required] |

### Return type

[**models::GetAdConversionDestination200Response**](getAdConversionDestination_200_response.md)

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


## update_forwarding_rule

> models::CreateForwardingRule201Response update_forwarding_rule(rule_id, update_forwarding_rule_request)
Change a forwarding rule's API secret

Replaces the `apiSecret` of a rule whose destination needs one, such as a Google Analytics data stream's Measurement Protocol API secret. Before saving, Zernio sends one hit to Google's validation server; Google does not confirm the secret itself, so check GA4 Realtime after the next events. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**rule_id** | **String** | The rule `id`. | [required] |
**update_forwarding_rule_request** | [**UpdateForwardingRuleRequest**](UpdateForwardingRuleRequest.md) |  | [required] |

### Return type

[**models::CreateForwardingRule201Response**](createForwardingRule_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

