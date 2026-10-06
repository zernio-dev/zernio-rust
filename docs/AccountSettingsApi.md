# \AccountSettingsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_instagram_ice_breakers**](AccountSettingsApi.md#delete_instagram_ice_breakers) | **DELETE** /v1/accounts/{accountId}/instagram-ice-breakers | Delete IG ice breakers
[**delete_messenger_get_started**](AccountSettingsApi.md#delete_messenger_get_started) | **DELETE** /v1/accounts/{accountId}/messenger-get-started | Delete FB Get Started button
[**delete_messenger_greeting**](AccountSettingsApi.md#delete_messenger_greeting) | **DELETE** /v1/accounts/{accountId}/messenger-greeting | Delete FB greeting text
[**delete_messenger_ice_breakers**](AccountSettingsApi.md#delete_messenger_ice_breakers) | **DELETE** /v1/accounts/{accountId}/messenger-ice-breakers | Delete FB ice breakers
[**delete_messenger_menu**](AccountSettingsApi.md#delete_messenger_menu) | **DELETE** /v1/accounts/{accountId}/messenger-menu | Delete persistent menu
[**delete_telegram_commands**](AccountSettingsApi.md#delete_telegram_commands) | **DELETE** /v1/accounts/{accountId}/telegram-commands | Delete TG bot commands
[**get_instagram_ice_breakers**](AccountSettingsApi.md#get_instagram_ice_breakers) | **GET** /v1/accounts/{accountId}/instagram-ice-breakers | Get IG ice breakers
[**get_messenger_get_started**](AccountSettingsApi.md#get_messenger_get_started) | **GET** /v1/accounts/{accountId}/messenger-get-started | Get FB Get Started button
[**get_messenger_greeting**](AccountSettingsApi.md#get_messenger_greeting) | **GET** /v1/accounts/{accountId}/messenger-greeting | Get FB greeting text
[**get_messenger_ice_breakers**](AccountSettingsApi.md#get_messenger_ice_breakers) | **GET** /v1/accounts/{accountId}/messenger-ice-breakers | Get FB ice breakers
[**get_messenger_menu**](AccountSettingsApi.md#get_messenger_menu) | **GET** /v1/accounts/{accountId}/messenger-menu | Get persistent menu
[**get_telegram_commands**](AccountSettingsApi.md#get_telegram_commands) | **GET** /v1/accounts/{accountId}/telegram-commands | Get TG bot commands
[**set_instagram_ice_breakers**](AccountSettingsApi.md#set_instagram_ice_breakers) | **PUT** /v1/accounts/{accountId}/instagram-ice-breakers | Set IG ice breakers
[**set_messenger_get_started**](AccountSettingsApi.md#set_messenger_get_started) | **PUT** /v1/accounts/{accountId}/messenger-get-started | Set FB Get Started button
[**set_messenger_greeting**](AccountSettingsApi.md#set_messenger_greeting) | **PUT** /v1/accounts/{accountId}/messenger-greeting | Set FB greeting text
[**set_messenger_ice_breakers**](AccountSettingsApi.md#set_messenger_ice_breakers) | **PUT** /v1/accounts/{accountId}/messenger-ice-breakers | Set FB ice breakers
[**set_messenger_menu**](AccountSettingsApi.md#set_messenger_menu) | **PUT** /v1/accounts/{accountId}/messenger-menu | Set persistent menu
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


## delete_messenger_greeting

> models::UpdateYoutubeDefaultPlaylist200Response delete_messenger_greeting(account_id)
Delete FB greeting text

Remove the greeting text from every locale.

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


## delete_messenger_ice_breakers

> models::UpdateYoutubeDefaultPlaylist200Response delete_messenger_ice_breakers(account_id)
Delete FB ice breakers

Remove the ice breakers from every locale.

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
Delete persistent menu

Removes the persistent menu from this Facebook Messenger or Instagram account.

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


## get_messenger_greeting

> models::GetMessengerGreeting200Response get_messenger_greeting(account_id)
Get FB greeting text

Get the greeting text a Facebook page shows on its Messenger welcome screen, one entry per locale. `data` is empty when the page has none.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |

### Return type

[**models::GetMessengerGreeting200Response**](getMessengerGreeting_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_messenger_ice_breakers

> models::GetMessengerIceBreakers200Response get_messenger_ice_breakers(account_id)
Get FB ice breakers

Get the ice breakers (FAQ questions shown when a person opens a new Messenger thread) for a Facebook page, one entry per locale. Instagram ice breakers live at /v1/accounts/{accountId}/instagram-ice-breakers.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |

### Return type

[**models::GetMessengerIceBreakers200Response**](getMessengerIceBreakers_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_messenger_menu

> models::GetMessengerMenu200Response get_messenger_menu(account_id)
Get persistent menu

Get the persistent menu configuration for a Facebook Messenger or Instagram account. Instagram accounts connected through Facebook Login are read through their linked Page (Meta's `platform=instagram`), Instagram Login accounts through the Instagram API.

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


## set_messenger_greeting

> models::UpdateYoutubeDefaultPlaylist200Response set_messenger_greeting(account_id, set_messenger_greeting_request)
Set FB greeting text

Set the greeting text on a Facebook page's Messenger welcome screen (Meta's `greeting` Messenger Profile field). One entry must use locale `default`; add more for other locales. Meta personalises `{{user_first_name}}`, `{{user_last_name}}` and `{{user_full_name}}`. Replaces every locale already set.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**set_messenger_greeting_request** | [**SetMessengerGreetingRequest**](SetMessengerGreetingRequest.md) |  | [required] |

### Return type

[**models::UpdateYoutubeDefaultPlaylist200Response**](updateYoutubeDefaultPlaylist_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## set_messenger_ice_breakers

> models::UpdateYoutubeDefaultPlaylist200Response set_messenger_ice_breakers(account_id, set_messenger_ice_breakers_request)
Set FB ice breakers

Set up to 4 ice breakers per locale for a Facebook page (Meta's `ice_breakers` Messenger Profile field). One entry must use locale `default`. A tap sends a postback with the question's `payload`, which arrives as `message.received` with `metadata.postbackPayload`; use `zernio:workflow:<workflowId>` to start a workflow (it must be active on this account and profile). Replaces every locale already set.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**set_messenger_ice_breakers_request** | [**SetMessengerIceBreakersRequest**](SetMessengerIceBreakersRequest.md) |  | [required] |

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
Set persistent menu

Set the persistent menu for a Facebook Messenger or Instagram account. Max 3 top-level items, max 5 nested items. On Facebook, Meta only shows a persistent menu on a page that has a Get Started button, so set one first with PUT /v1/accounts/{accountId}/messenger-get-started. A postback button whose payload is `zernio:workflow:<workflowId>` starts that workflow when tapped; the workflow must be active on this account and profile.

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

