# \DiscordApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_discord_channels**](DiscordApi.md#get_discord_channels) | **GET** /v1/accounts/{accountId}/discord-channels | List Discord guild channels
[**get_discord_settings**](DiscordApi.md#get_discord_settings) | **GET** /v1/accounts/{accountId}/discord-settings | Get Discord account settings
[**update_discord_settings**](DiscordApi.md#update_discord_settings) | **PATCH** /v1/accounts/{accountId}/discord-settings | Update Discord settings



## get_discord_channels

> models::GetDiscordChannels200Response get_discord_channels(account_id)
List Discord guild channels

Returns the text, announcement, and forum channels in the connected Discord guild. Use this to discover available channels when switching the connected channel via PATCH /v1/accounts/{accountId}/discord-settings.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |

### Return type

[**models::GetDiscordChannels200Response**](getDiscordChannels_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_discord_settings

> models::GetDiscordSettings200Response get_discord_settings(account_id)
Get Discord account settings

Returns the current Discord account settings including webhook identity (display name and avatar), connected channel, and guild information.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |

### Return type

[**models::GetDiscordSettings200Response**](getDiscordSettings_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_discord_settings

> models::UpdateDiscordSettings200Response update_discord_settings(account_id, update_discord_settings_request)
Update Discord settings

Update Discord account settings. Supports two operations (can be combined):  1. **Webhook identity** - Set the default display name and avatar that appear as the message author on every post. These are account-level defaults; individual posts can override them via platformSpecificData.webhookUsername / webhookAvatarUrl.  2. **Switch channel** - Move the connection to a different channel in the same guild. A new webhook is automatically created in the target channel. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**update_discord_settings_request** | [**UpdateDiscordSettingsRequest**](UpdateDiscordSettingsRequest.md) |  | [required] |

### Return type

[**models::UpdateDiscordSettings200Response**](updateDiscordSettings_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

