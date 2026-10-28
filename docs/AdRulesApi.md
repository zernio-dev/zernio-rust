# \AdRulesApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_ad_rule**](AdRulesApi.md#create_ad_rule) | **POST** /v1/ads/rules | Create an ad rule
[**delete_ad_rule**](AdRulesApi.md#delete_ad_rule) | **DELETE** /v1/ads/rules/{ruleId} | Delete an ad rule
[**get_ad_rule**](AdRulesApi.md#get_ad_rule) | **GET** /v1/ads/rules/{ruleId} | Get an ad rule
[**list_ad_rule_activity**](AdRulesApi.md#list_ad_rule_activity) | **GET** /v1/ads/rules/activity | List every change ad rules made
[**list_ad_rule_runs**](AdRulesApi.md#list_ad_rule_runs) | **GET** /v1/ads/rules/{ruleId}/runs | List an ad rule's runs
[**list_ad_rules**](AdRulesApi.md#list_ad_rules) | **GET** /v1/ads/rules | List ad rules
[**preview_ad_rule**](AdRulesApi.md#preview_ad_rule) | **POST** /v1/ads/rules/{ruleId}/preview | Preview an ad rule
[**update_ad_rule**](AdRulesApi.md#update_ad_rule) | **PATCH** /v1/ads/rules/{ruleId} | Update an ad rule



## create_ad_rule

> models::CreateAdRule201Response create_ad_rule(create_ad_rule_request)
Create an ad rule

Creates a rule that checks the campaigns or ad sets of one ad account on a schedule and acts on each one that meets every condition.  Rules support Meta, Google, TikTok, LinkedIn, Pinterest, X and Reddit ads connections. Each campaign or ad set is evaluated on its own, over the ad account's calendar days, from the metrics Zernio syncs. A rule can notify (the `ad_rule.triggered` webhook), and take at most one of `pause`, `activate` and `adjust_budget`. After acting on an object, the rule leaves that object alone for `cooldownMinutes`; a rule that pauses, activates or adjusts budgets needs a cooldown at least as long as its schedule.  `activate` only reactivates objects a rule paused, never ones you paused yourself, and only once the cooldown has passed since that pause. If you reactivate and pause such an object yourself between two runs of a rule, Zernio cannot tell your pause from the rule's, and an `activate` rule may reactivate it.  Use `POST /v1/ads/rules/{ruleId}/preview` to see what a rule would match before enabling it. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_ad_rule_request** | [**CreateAdRuleRequest**](CreateAdRuleRequest.md) |  | [required] |

### Return type

[**models::CreateAdRule201Response**](createAdRule_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_ad_rule

> models::UpdateYoutubeDefaultPlaylist200Response delete_ad_rule(rule_id)
Delete an ad rule

Deletes a rule and its run history. Changes the rule already made on the platform stay. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**rule_id** | **String** |  | [required] |

### Return type

[**models::UpdateYoutubeDefaultPlaylist200Response**](updateYoutubeDefaultPlaylist_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad_rule

> models::CreateAdRule201Response get_ad_rule(rule_id)
Get an ad rule

Returns one ad rule. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**rule_id** | **String** |  | [required] |

### Return type

[**models::CreateAdRule201Response**](createAdRule_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ad_rule_activity

> models::ListAdRuleActivity200Response list_ad_rule_activity(rule_id, account_id, r#type, from, to, limit, cursor)
List every change ad rules made

The permanent record of what your rules did: one entry per pause, reactivation or budget change (including skipped and failed attempts), newest first, across all rules of the profiles the key can reach. Entries stay after a rule is renamed or deleted; `ruleName` is the rule's name when it acted. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**rule_id** | Option<**String**> |  |  |
**account_id** | Option<**String**> | Only changes of rules on this ads connection. |  |
**r#type** | Option<**String**> |  |  |
**from** | Option<**String**> | ISO 8601 date-time, inclusive. |  |
**to** | Option<**String**> | ISO 8601 date-time, inclusive. |  |
**limit** | Option<**i32**> |  |  |[default to 50]
**cursor** | Option<**String**> | `nextCursor` from the previous page. |  |

### Return type

[**models::ListAdRuleActivity200Response**](listAdRuleActivity_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ad_rule_runs

> models::ListAdRuleRuns200Response list_ad_rule_runs(rule_id, limit, skip)
List an ad rule's runs

Lists a rule's scheduled runs, newest first: what each run evaluated, matched and did. Runs that changed something (or tried to) are kept permanently, also after the rule is deleted; runs that changed nothing are dropped after about 31 days. For every change across all rules, use `GET /v1/ads/rules/activity`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**rule_id** | **String** |  | [required] |
**limit** | Option<**i32**> |  |  |[default to 20]
**skip** | Option<**i32**> |  |  |[default to 0]

### Return type

[**models::ListAdRuleRuns200Response**](listAdRuleRuns_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ad_rules

> models::ListAdRules200Response list_ad_rules(account_id, ad_account_id, limit, skip)
List ad rules

Lists the ad rules on the profiles your key can reach, newest first. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | Option<**String**> | Only rules on this ads connection. |  |
**ad_account_id** | Option<**String**> | Only rules watching this platform ad account. |  |
**limit** | Option<**i32**> |  |  |[default to 50]
**skip** | Option<**i32**> |  |  |[default to 0]

### Return type

[**models::ListAdRules200Response**](listAdRules_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## preview_ad_rule

> models::AdRuleEvaluation preview_ad_rule(rule_id)
Preview an ad rule

Evaluates a rule against current metrics and returns what it would match right now, without acting on anything, sending a webhook or starting a cooldown. Works on disabled rules. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**rule_id** | **String** |  | [required] |

### Return type

[**models::AdRuleEvaluation**](AdRuleEvaluation.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_ad_rule

> models::CreateAdRule201Response update_ad_rule(rule_id, update_ad_rule_request)
Update an ad rule

Changes any field of a rule except its connection and ad account. Send `campaignIds: null` to check the whole ad account again. Changing the schedule, or enabling a disabled rule, moves the next run; re-sending `enabled: true` on an enabled rule does not. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**rule_id** | **String** |  | [required] |
**update_ad_rule_request** | [**UpdateAdRuleRequest**](UpdateAdRuleRequest.md) |  | [required] |

### Return type

[**models::CreateAdRule201Response**](createAdRule_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

