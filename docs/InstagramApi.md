# \InstagramApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_instagram_publishing_limit**](InstagramApi.md#get_instagram_publishing_limit) | **GET** /v1/accounts/{accountId}/instagram/publishing-limit | Get Instagram publishing limit
[**get_instagram_story_insights**](InstagramApi.md#get_instagram_story_insights) | **GET** /v1/accounts/{accountId}/instagram/stories/{storyId}/insights | Get Instagram story insights
[**list_instagram_stories**](InstagramApi.md#list_instagram_stories) | **GET** /v1/accounts/{accountId}/instagram/stories | List active Instagram stories



## get_instagram_publishing_limit

> models::GetInstagramPublishingLimit200Response get_instagram_publishing_limit(account_id)
Get Instagram publishing limit

Returns the account's remaining content-publishing quota for Instagram's rolling 24-hour window, so you can pace publishing and warn before the cap is reached.  `quotaUsage` counts containers published since the start of the window. Always compare against the returned `quotaTotal` rather than hardcoding a number: Meta's prose documentation and the live API disagree on the value, and the live value is authoritative. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The ID of the Instagram account | [required] |

### Return type

[**models::GetInstagramPublishingLimit200Response**](getInstagramPublishingLimit_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_instagram_story_insights

> models::GetInstagramStoryInsights200Response get_instagram_story_insights(account_id, story_id)
Get Instagram story insights

Returns metrics for a single story. The `source` field discriminates between three states:  - `live` — fetched from Meta in real time (story is still active) - `cached` — fetched from a persisted `story_insights` webhook payload   (story has expired but we received its final-state metrics from Meta) - `unavailable` — story has expired and we never received its webhook   payload (for example, the account connected after the story expired)  Field semantics follow Meta's API. Counts below 5 may be returned as 0 due to Meta's privacy floor on small audiences. The `navigation` field is the sum of `tapsForward + tapsBack + exits + swipesForward`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Instagram account ID | [required] |
**story_id** | **String** | The Instagram media ID of the story. | [required] |

### Return type

[**models::GetInstagramStoryInsights200Response**](getInstagramStoryInsights_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_instagram_stories

> models::ListInstagramStories200Response list_instagram_stories(account_id)
List active Instagram stories

Returns the IG Business/Creator account's currently-active stories. Meta keeps stories live for 24h; expired stories are not returned.  Limitations propagated from Meta (these are NOT bugs): - 24h window only - Live videos excluded - Reshared stories not returned - `mediaUrl` may be null if Meta flagged the story for copyright - `caption`, `likeCount`, `commentsCount` do not apply to story media 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Instagram account ID | [required] |

### Return type

[**models::ListInstagramStories200Response**](listInstagramStories_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

