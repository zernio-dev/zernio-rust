# \AccountsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_account**](AccountsApi.md#delete_account) | **DELETE** /v1/accounts/{accountId} | Disconnect account
[**get_account_health**](AccountsApi.md#get_account_health) | **GET** /v1/accounts/{accountId}/health | Check account health
[**get_all_accounts_health**](AccountsApi.md#get_all_accounts_health) | **GET** /v1/accounts/health | Check accounts health
[**get_follower_stats**](AccountsApi.md#get_follower_stats) | **GET** /v1/accounts/follower-stats | Get follower stats
[**get_instagram_follow_status**](AccountsApi.md#get_instagram_follow_status) | **GET** /v1/accounts/{accountId}/follow-status/{userId} | Check whether an Instagram user follows the account
[**get_slack_settings**](AccountsApi.md#get_slack_settings) | **GET** /v1/accounts/{accountId}/slack-settings | Get Slack account settings
[**get_tik_tok_creator_info**](AccountsApi.md#get_tik_tok_creator_info) | **GET** /v1/accounts/{accountId}/tiktok/creator-info | Get TikTok creator info
[**list_accounts**](AccountsApi.md#list_accounts) | **GET** /v1/accounts | List accounts
[**move_account_to_profile**](AccountsApi.md#move_account_to_profile) | **PATCH** /v1/accounts/{accountId} | Move account to another profile
[**update_account**](AccountsApi.md#update_account) | **PUT** /v1/accounts/{accountId} | Update account
[**update_slack_settings**](AccountsApi.md#update_slack_settings) | **PATCH** /v1/accounts/{accountId}/slack-settings | Update Slack account settings



## delete_account

> models::DeleteAccountGroup200Response delete_account(account_id)
Disconnect account

Disconnects and removes a connected social account.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |

### Return type

[**models::DeleteAccountGroup200Response**](deleteAccountGroup_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_account_health

> models::GetAccountHealth200Response get_account_health(account_id)
Check account health

Returns detailed health info for a specific account including token status, permissions, and recommendations.  For WhatsApp accounts the response also includes `platformConnection`, a live probe of the Meta link behind the channel (the same read as `GET /v1/whatsapp/number-info`). The OAuth token can be perfectly valid while Meta refuses to serve the phone-number object (for example after a phone-side coexistence disconnect), so `tokenStatus` alone is not a liveness signal for WhatsApp. When the Meta link is dead, `platformConnection.status` is `disconnected` and the overall `status` is `error`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The account ID to check | [required] |

### Return type

[**models::GetAccountHealth200Response**](getAccountHealth_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_all_accounts_health

> models::GetAllAccountsHealth200Response get_all_accounts_health(profile_id, platform, status)
Check accounts health

Returns health status of all connected accounts including token validity, permissions, and issues needing attention.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | Option<**String**> | Filter by profile ID |  |
**platform** | Option<**String**> | Filter by platform |  |
**status** | Option<**String**> | Filter by health status |  |

### Return type

[**models::GetAllAccountsHealth200Response**](getAllAccountsHealth_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_follower_stats

> models::FollowerStatsResponse get_follower_stats(account_ids, profile_id, from_date, to_date, granularity)
Get follower stats

Returns follower count history and growth metrics for connected social accounts. Requires analytics add-on subscription. Follower counts are refreshed once per day. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_ids** | Option<**String**> | Comma-separated list of account IDs (optional, defaults to all user's accounts) |  |
**profile_id** | Option<**String**> | Filter by profile ID |  |
**from_date** | Option<**String**> | Start date in YYYY-MM-DD format (defaults to 30 days ago) |  |
**to_date** | Option<**String**> | End date in YYYY-MM-DD format (defaults to today) |  |
**granularity** | Option<**String**> | Data aggregation level |  |[default to daily]

### Return type

[**models::FollowerStatsResponse**](FollowerStatsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_instagram_follow_status

> models::GetInstagramFollowStatus200Response get_instagram_follow_status(account_id, user_id, refresh)
Check whether an Instagram user follows the account

Resolves the follow relationship between an Instagram user and the connected account, plus their public profile counters.  `userId` is the Instagram-scoped id (IGSID) Meta gives you on a webhook: `sender.id` on `message.received`, `comment.author.id` on `comment.received`.  **Meta only answers for people who have MESSAGED the account.** Commenting grants no consent, so a commenter who has never DMed you is unresolvable - that is a platform rule, not a limitation of this endpoint. When it cannot be resolved the response is still `200` with `isFollower: null` and an `unavailableReason`, because \"unknown\" is a normal state to branch on:    * `consent_required` - the user has never messaged this account.   * `dm_access_disabled` - the account owner turned off Instagram Direct API access.   * `not_messageable` - the id is not a messaging-scoped id.   * `error` - a transient Graph API failure.  To gate a comment automation on this, use the automation's `audience` rules instead of calling this per comment - they run the same lookup only on comments that actually match a keyword, and can ask the commenter to confirm with one tap.  Answers are cached briefly per (account, user). Pass `refresh=true` right after asking someone to follow, so a follow from a moment ago is visible. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Instagram account ID | [required] |
**user_id** | **String** | Instagram-scoped user id (IGSID) from a webhook payload | [required] |
**refresh** | Option<**bool**> | Bypass the cache and re-query Meta |  |

### Return type

[**models::GetInstagramFollowStatus200Response**](getInstagramFollowStatus_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_slack_settings

> models::GetSlackSettings200Response get_slack_settings(account_id)
Get Slack account settings

Returns the connected Slack channel details and the default message identity (name and avatar shown as the author on every post, with Slack's APP badge). The identity applies to messages only; the app's own Slack profile is global and cannot be changed per workspace.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |

### Return type

[**models::GetSlackSettings200Response**](getSlackSettings_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_tik_tok_creator_info

> models::GetTikTokCreatorInfo200Response get_tik_tok_creator_info(account_id, media_type)
Get TikTok creator info

Returns TikTok creator details, available privacy levels, posting limits, and commercial content options for a specific TikTok account. Only works with TikTok accounts.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The TikTok account ID | [required] |
**media_type** | Option<**String**> | The media type to get creator info for (affects available interaction settings) |  |[default to video]

### Return type

[**models::GetTikTokCreatorInfo200Response**](getTikTokCreatorInfo_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_accounts

> models::AccountsListResponse list_accounts(profile_id, platform, status, include_over_limit, page, limit)
List accounts

Returns connected social accounts. Only includes accounts within the plan limit by default. Follower data requires analytics add-on. Supports optional server-side pagination via page/limit params. When omitted, returns all accounts (backward-compatible). page and limit must be supplied together; out-of-range page/limit values are rejected with 400 rather than silently clamped. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | Option<**String**> | Filter accounts by profile ID. Must be a valid ObjectId. |  |
**platform** | Option<**String**> | Filter accounts by platform (e.g. \"instagram\", \"twitter\"). |  |
**status** | Option<**String**> | Filter accounts by connection status. `connected` returns healthy accounts; `disconnected` returns accounts that need reconnection (per the same reconnection check surfaced in the dashboard). Omit to return accounts in any status. When combined with page/limit, pagination totals reflect the filtered result set.  |  |
**include_over_limit** | Option<**bool**> | When true, includes accounts from over-limit profiles. |  |[default to false]
**page** | Option<**i32**> | Page number (1-based). Must be provided together with limit to enable server-side pagination; sending only one of the two returns 400. Omit both for all accounts.  |  |
**limit** | Option<**i32**> | Page size. Must be provided together with page; sending only one of the two returns 400.  |  |

### Return type

[**models::AccountsListResponse**](AccountsListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## move_account_to_profile

> models::MoveAccountToProfile200Response move_account_to_profile(account_id, move_account_to_profile_request)
Move account to another profile

Moves a connected social account to a different profile owned by the same user. The target profile must belong to the same user as the account.  For API keys restricted to specific profiles, BOTH the source account's current profile AND the target profile must be in the key's allowed set. Calls with a target profile outside the key's scope return 403. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**move_account_to_profile_request** | [**MoveAccountToProfileRequest**](MoveAccountToProfileRequest.md) |  | [required] |

### Return type

[**models::MoveAccountToProfile200Response**](moveAccountToProfile_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_account

> models::UpdateAccount200Response update_account(account_id, update_account_request)
Update account

Updates a connected social account's display name or username override.  For X/Twitter accounts on usage-based billing, also accepts an `xCapabilities` object to toggle background API operations that incur X API pass-through costs. Both fields are opt-in (default `false`) — when off, no analytics syncs or DM polling are performed for that account, and no API call is metered for those operations. Publishing and deleting posts are always available regardless of these toggles. Setting `xCapabilities` on a non-X account returns 400. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**update_account_request** | [**UpdateAccountRequest**](UpdateAccountRequest.md) |  | [required] |

### Return type

[**models::UpdateAccount200Response**](updateAccount_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_slack_settings

> update_slack_settings(account_id, update_slack_settings_request)
Update Slack account settings

Set or clear the default message identity for this channel. Empty string clears a field; per-post platformSpecificData.username/iconUrl still override these defaults.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**update_slack_settings_request** | [**UpdateSlackSettingsRequest**](UpdateSlackSettingsRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

