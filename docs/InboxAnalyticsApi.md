# \InboxAnalyticsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_inbox_conversation_analytics**](InboxAnalyticsApi.md#get_inbox_conversation_analytics) | **GET** /v1/analytics/inbox/conversations/{conversationId} | Get conversation analytics
[**get_inbox_heatmap**](InboxAnalyticsApi.md#get_inbox_heatmap) | **GET** /v1/analytics/inbox/heatmap | Get day × hour heatmap
[**get_inbox_response_time**](InboxAnalyticsApi.md#get_inbox_response_time) | **GET** /v1/analytics/inbox/response-time | Get inbox response-time stats
[**get_inbox_source_breakdown**](InboxAnalyticsApi.md#get_inbox_source_breakdown) | **GET** /v1/analytics/inbox/source-breakdown | Get inbox source breakdown
[**get_inbox_top_accounts**](InboxAnalyticsApi.md#get_inbox_top_accounts) | **GET** /v1/analytics/inbox/top-accounts | Get top accounts by inbox volume
[**get_inbox_volume**](InboxAnalyticsApi.md#get_inbox_volume) | **GET** /v1/analytics/inbox/volume | Get inbox messaging volume
[**list_inbox_conversation_analytics**](InboxAnalyticsApi.md#list_inbox_conversation_analytics) | **GET** /v1/analytics/inbox/conversations | List conversation analytics



## get_inbox_conversation_analytics

> models::GetInboxConversationAnalytics200Response get_inbox_conversation_analytics(conversation_id, from_date, to_date)
Get conversation analytics

Per-conversation inbox analytics. The inbox analog of /v1/analytics/post-timeline — one conversation, daily totals, source mix.  The {conversationId} path param accepts EITHER the Mongo `_id` of the Conversation document OR its `platformConversationId` (the same identity used by metadata.conversationId at ingest time). Ownership is verified in MongoDB against the caller's team before the Tinybird query fires.  Max date range is 365 days. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** | Mongo _id or platformConversationId. | [required] |
**from_date** | **String** |  | [required] |
**to_date** | Option<**String**> |  |  |

### Return type

[**models::GetInboxConversationAnalytics200Response**](getInboxConversationAnalytics_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_inbox_heatmap

> models::GetInboxHeatmap200Response get_inbox_heatmap(from_date, to_date, profile_id, platform, account_id, source, action)
Get day × hour heatmap

Day-of-week × hour-of-day breakdown of inbox messages. Buckets are sparse — only cells with at least one event are returned; clients zero-fill the rest to render the full 7×24 grid. The `dow` field follows ClickHouse's `toDayOfWeek` convention (1 = Monday … 7 = Sunday). Max date range is 365 days. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**from_date** | **String** |  | [required] |
**to_date** | Option<**String**> |  |  |
**profile_id** | Option<**String**> |  |  |
**platform** | Option<**String**> |  |  |
**account_id** | Option<**String**> |  |  |
**source** | Option<**String**> |  |  |
**action** | Option<**String**> | Narrow to a single event type. \"all\" or omitted means no filter. |  |

### Return type

[**models::GetInboxHeatmap200Response**](getInboxHeatmap_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_inbox_response_time

> models::GetInboxResponseTime200Response get_inbox_response_time(from_date, to_date, profile_id, platform, account_id)
Get inbox response-time stats

Time-to-first-response stats. Pairs each received message with the next sent message in the same conversation and reports the delta as both summary statistics and a fixed-bucket histogram suited for the analytics page's TTR chart.  `sampleSize` reflects only conversations that received AND got a reply in the window — received-but-never-answered conversations are excluded. Compare against /v1/analytics/inbox/volume's `summary.received` to compute reply rate.  Max date range is 365 days. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**from_date** | **String** |  | [required] |
**to_date** | Option<**String**> |  |  |
**profile_id** | Option<**String**> |  |  |
**platform** | Option<**String**> |  |  |
**account_id** | Option<**String**> |  |  |

### Return type

[**models::GetInboxResponseTime200Response**](getInboxResponseTime_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_inbox_source_breakdown

> models::GetInboxSourceBreakdown200Response get_inbox_source_breakdown(from_date, to_date, profile_id, platform, account_id)
Get inbox source breakdown

Breakdown of inbox messages by their lineage source (the `metadata.source` field set at ingest time: human / workflow / sequence / broadcast / comment_automation / api / contact / platform). Each source row also carries a per-platform sub-split. Max date range is 365 days. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**from_date** | **String** |  | [required] |
**to_date** | Option<**String**> |  |  |
**profile_id** | Option<**String**> |  |  |
**platform** | Option<**String**> |  |  |
**account_id** | Option<**String**> |  |  |

### Return type

[**models::GetInboxSourceBreakdown200Response**](getInboxSourceBreakdown_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_inbox_top_accounts

> models::GetInboxTopAccounts200Response get_inbox_top_accounts(from_date, to_date, profile_id, platform, source, limit)
Get top accounts by inbox volume

Leaderboard of social accounts by inbox message volume. Decorates each row with display labels from the live SocialAccount record (so the UI shows username + displayName, not just an ID). Accounts that no longer map to a SocialAccount surface as \"(disconnected)\" so the row stays visible. Max date range is 365 days. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**from_date** | **String** |  | [required] |
**to_date** | Option<**String**> |  |  |
**profile_id** | Option<**String**> |  |  |
**platform** | Option<**String**> |  |  |
**source** | Option<**String**> |  |  |
**limit** | Option<**i32**> | Cap on returned rows. Lower than the posting listing's 100 because each row triggers a SocialAccount Mongo lookup. |  |[default to 10]

### Return type

[**models::GetInboxTopAccounts200Response**](getInboxTopAccounts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_inbox_volume

> models::GetInboxVolume200Response get_inbox_volume(from_date, to_date, profile_id, platform, account_id, source)
Get inbox messaging volume

Daily inbox messaging volume + breakdowns. Folds the raw messaging events into three projections so the client can render the volume chart, KPI strip, and per-platform stacked bar from a single call. Max date range is 365 days. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**from_date** | **String** | Inclusive lower bound (YYYY-MM-DD). Required. | [required] |
**to_date** | Option<**String**> | Inclusive upper bound (YYYY-MM-DD). Defaults to today. |  |
**profile_id** | Option<**String**> |  |  |
**platform** | Option<**String**> | Filter by single platform (facebook, instagram, twitter, etc.). |  |
**account_id** | Option<**String**> |  |  |
**source** | Option<**String**> | Filter by metadata.source lineage (human, workflow, sequence, broadcast, comment_automation, api, contact, platform). |  |

### Return type

[**models::GetInboxVolume200Response**](getInboxVolume_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_inbox_conversation_analytics

> models::ListInboxConversationAnalytics200Response list_inbox_conversation_analytics(from_date, to_date, profile_id, platform, account_id, source, limit, page, sort_by, order)
List conversation analytics

Per-conversation listing with per-row totals + first/last message timestamps. The inbox analog of GET /v1/analytics (posts listing) — same filter shape, same pagination, same sort/order semantics. Use as the entry point for the per-conversation analytics drawer at /v1/analytics/inbox/conversations/{conversationId}.  Rows are enriched with the conversation's participant info (`participantName`, `participantUsername`, `participantPicture`) and last-message preview by joining the Conversation document scoped to the caller's team. Max date range is 365 days. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**from_date** | **String** |  | [required] |
**to_date** | Option<**String**> |  |  |
**profile_id** | Option<**String**> |  |  |
**platform** | Option<**String**> |  |  |
**account_id** | Option<**String**> |  |  |
**source** | Option<**String**> |  |  |
**limit** | Option<**i32**> |  |  |[default to 50]
**page** | Option<**i32**> |  |  |[default to 1]
**sort_by** | Option<**String**> |  |  |[default to lastMessageAt]
**order** | Option<**String**> |  |  |[default to desc]

### Return type

[**models::ListInboxConversationAnalytics200Response**](listInboxConversationAnalytics_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

