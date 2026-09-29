# \AccountSettingsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_instagram_ice_breakers**](AccountSettingsApi.md#delete_instagram_ice_breakers) | **DELETE** /v1/accounts/{accountId}/instagram-ice-breakers | Delete IG ice breakers
[**delete_messenger_get_started**](AccountSettingsApi.md#delete_messenger_get_started) | **DELETE** /v1/accounts/{accountId}/messenger-get-started | Delete FB Get Started button
[**delete_messenger_menu**](AccountSettingsApi.md#delete_messenger_menu) | **DELETE** /v1/accounts/{accountId}/messenger-menu | Delete FB persistent menu
[**delete_telegram_commands**](AccountSettingsApi.md#delete_telegram_commands) | **DELETE** /v1/accounts/{accountId}/telegram-commands | Delete TG bot commands
[**get_instagram_ice_breakers**](AccountSettingsApi.md#get_instagram_ice_breakers) | **GET** /v1/accounts/{accountId}/instagram-ice-breakers | Get IG ice breakers
[**get_messenger_get_started**](AccountSettingsApi.md#get_messenger_get_started) | **GET** /v1/accounts/{accountId}/messenger-get-started | Get FB Get Started button
[**get_messenger_menu**](AccountSettingsApi.md#get_messenger_menu) | **GET** /v1/accounts/{accountId}/messenger-menu | Get FB persistent menu
[**get_telegram_commands**](AccountSettingsApi.md#get_telegram_commands) | **GET** /v1/accounts/{accountId}/telegram-commands | Get TG bot commands
[**set_instagram_ice_breakers**](AccountSettingsApi.md#set_instagram_ice_breakers) | **PUT** /v1/accounts/{accountId}/instagram-ice-breakers | Set IG ice breakers
[**set_messenger_get_started**](AccountSettingsApi.md#set_messenger_get_started) | **PUT** /v1/accounts/{accountId}/messenger-get-started | Set FB Get Started button
[**set_messenger_menu**](AccountSettingsApi.md#set_messenger_menu) | **PUT** /v1/accounts/{accountId}/messenger-menu | Set FB persistent menu
[**set_telegram_commands**](AccountSettingsApi.md#set_telegram_commands) | **PUT** /v1/accounts/{accountId}/telegram-commands | Set TG bot commands



## delete_instagram_ice_breakers

> delete_instagram_ice_breakers(account_id)
Delete IG ice breakers

Removes the ice breaker questions from an Instagram account's Messenger experience.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_messenger_get_started

> models::UpdateYoutubeDefaultPlaylist200Response delete_messenger_get_started(account_id)
Delete FB Get Started button

Remove the Get Started button. Meta refuses while a persistent menu is set, so delete the menu first.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |

### Return type

[**models::UpdateYoutubeDefaultPlaylist200Response**](updateYoutubeDefaultPlaylist_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_messenger_menu

> delete_messenger_menu(account_id)
Delete FB persistent menu

Removes the persistent menu from Facebook Messenger conversations for this account.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_telegram_commands

> delete_telegram_commands(account_id)
Delete TG bot commands

Clears all bot commands configured for a Telegram bot account.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_instagram_ice_breakers

> models::GetMessengerMenu200Response get_instagram_ice_breakers(account_id)
Get IG ice breakers

Get the ice breaker configuration for an Instagram account.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |

### Return type

[**models::GetMessengerMenu200Response**](getMessengerMenu_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_messenger_get_started

> models::GetMessengerGetStarted200Response get_messenger_get_started(account_id)
Get FB Get Started button

Get the Get Started button payload for a Facebook Messenger account. `data` is null when the page has none.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |

### Return type

[**models::GetMessengerGetStarted200Response**](getMessengerGetStarted_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_messenger_menu

> models::GetMessengerMenu200Response get_messenger_menu(account_id)
Get FB persistent menu

Get the persistent menu configuration for a Facebook Messenger account.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |

### Return type

[**models::GetMessengerMenu200Response**](getMessengerMenu_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_telegram_commands

> models::GetTelegramCommands200Response get_telegram_commands(account_id)
Get TG bot commands

Get the bot commands configuration for a Telegram account.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |

### Return type

[**models::GetTelegramCommands200Response**](getTelegramCommands_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## set_instagram_ice_breakers

> set_instagram_ice_breakers(account_id, set_instagram_ice_breakers_request)
Set IG ice breakers

Set ice breakers for an Instagram account. Max 4 ice breakers, question max 80 chars.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**set_instagram_ice_breakers_request** | [**SetInstagramIceBreakersRequest**](SetInstagramIceBreakersRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## set_messenger_get_started

> models::UpdateYoutubeDefaultPlaylist200Response set_messenger_get_started(account_id, set_messenger_get_started_request)
Set FB Get Started button

Set the Get Started button shown on a Facebook page's Messenger welcome screen. Meta requires it before a persistent menu can be set. Tapping it sends a postback with `payload`, which arrives as a `message.received` webhook carrying it in `metadata.postbackPayload`. Use `zernio:workflow:<workflowId>` to start a workflow on the tap; the workflow must be active on this account and profile.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**set_messenger_get_started_request** | [**SetMessengerGetStartedRequest**](SetMessengerGetStartedRequest.md) |  | [required] |

### Return type

[**models::UpdateYoutubeDefaultPlaylist200Response**](updateYoutubeDefaultPlaylist_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## set_messenger_menu

> set_messenger_menu(account_id, set_messenger_menu_request)
Set FB persistent menu

Set the persistent menu for a Facebook Messenger account. Max 3 top-level items, max 5 nested items. Meta only shows a persistent menu on a page that has a Get Started button, so set one first with PUT /v1/accounts/{accountId}/messenger-get-started. A postback button whose payload is `zernio:workflow:<workflowId>` starts that workflow when tapped; the workflow must be active on this account and profile.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**set_messenger_menu_request** | [**SetMessengerMenuRequest**](SetMessengerMenuRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## set_telegram_commands

> set_telegram_commands(account_id, set_telegram_commands_request)
Set TG bot commands

Set bot commands for a Telegram account.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**set_telegram_commands_request** | [**SetTelegramCommandsRequest**](SetTelegramCommandsRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

