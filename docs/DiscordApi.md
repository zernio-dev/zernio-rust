# \DiscordApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_discord_member_role**](DiscordApi.md#add_discord_member_role) | **PUT** /v1/discord/guilds/{guildId}/members/{userId}/roles/{roleId} | Assign a role to a guild member
[**create_discord_guild_role**](DiscordApi.md#create_discord_guild_role) | **POST** /v1/discord/guilds/{guildId}/roles | Create a Discord guild role
[**create_discord_scheduled_event**](DiscordApi.md#create_discord_scheduled_event) | **POST** /v1/discord/guilds/{guildId}/events | Create a Discord scheduled event
[**create_discord_thread**](DiscordApi.md#create_discord_thread) | **POST** /v1/discord/channels/{channelId}/threads | Create a Discord public thread
[**crosspost_discord_message**](DiscordApi.md#crosspost_discord_message) | **POST** /v1/discord/channels/{channelId}/messages/{messageId}/crosspost | Crosspost Discord message
[**delete_discord_guild_role**](DiscordApi.md#delete_discord_guild_role) | **DELETE** /v1/discord/guilds/{guildId}/roles/{roleId} | Delete a Discord guild role
[**delete_discord_message**](DiscordApi.md#delete_discord_message) | **DELETE** /v1/discord/channels/{channelId}/messages/{messageId} | Delete a Discord channel message
[**delete_discord_scheduled_event**](DiscordApi.md#delete_discord_scheduled_event) | **DELETE** /v1/discord/guilds/{guildId}/events/{eventId} | Delete a Discord scheduled event
[**edit_discord_guild_role**](DiscordApi.md#edit_discord_guild_role) | **PATCH** /v1/discord/guilds/{guildId}/roles/{roleId} | Edit a Discord guild role
[**get_discord_channels**](DiscordApi.md#get_discord_channels) | **GET** /v1/accounts/{accountId}/discord-channels | List Discord guild channels
[**get_discord_guild_member**](DiscordApi.md#get_discord_guild_member) | **GET** /v1/discord/guilds/{guildId}/members/{userId} | Get a Discord guild member
[**get_discord_scheduled_event**](DiscordApi.md#get_discord_scheduled_event) | **GET** /v1/discord/guilds/{guildId}/events/{eventId} | Get a Discord scheduled event
[**get_discord_settings**](DiscordApi.md#get_discord_settings) | **GET** /v1/accounts/{accountId}/discord-settings | Get Discord account settings
[**list_discord_guild_members**](DiscordApi.md#list_discord_guild_members) | **GET** /v1/discord/guilds/{guildId}/members | List Discord guild members
[**list_discord_guild_roles**](DiscordApi.md#list_discord_guild_roles) | **GET** /v1/discord/guilds/{guildId}/roles | List Discord guild roles
[**list_discord_pinned_messages**](DiscordApi.md#list_discord_pinned_messages) | **GET** /v1/discord/channels/{channelId}/pins | List pinned messages
[**list_discord_scheduled_events**](DiscordApi.md#list_discord_scheduled_events) | **GET** /v1/discord/guilds/{guildId}/events | List Discord scheduled events
[**pin_discord_message**](DiscordApi.md#pin_discord_message) | **PUT** /v1/discord/channels/{channelId}/pins/{messageId} | Pin a Discord message
[**remove_discord_member_role**](DiscordApi.md#remove_discord_member_role) | **DELETE** /v1/discord/guilds/{guildId}/members/{userId}/roles/{roleId} | Remove a role from a guild member
[**search_discord_guild_members**](DiscordApi.md#search_discord_guild_members) | **GET** /v1/discord/guilds/{guildId}/members/search | Search Discord guild members
[**send_discord_direct_message**](DiscordApi.md#send_discord_direct_message) | **POST** /v1/discord/dms | Send a Discord Direct Message
[**unpin_discord_message**](DiscordApi.md#unpin_discord_message) | **DELETE** /v1/discord/channels/{channelId}/pins/{messageId} | Unpin a Discord message
[**update_discord_scheduled_event**](DiscordApi.md#update_discord_scheduled_event) | **PATCH** /v1/discord/guilds/{guildId}/events/{eventId} | Update a Discord scheduled event
[**update_discord_settings**](DiscordApi.md#update_discord_settings) | **PATCH** /v1/accounts/{accountId}/discord-settings | Update Discord settings



## add_discord_member_role

> models::AddDiscordMemberRole200Response add_discord_member_role(guild_id, user_id, role_id, account_id)
Assign a role to a guild member

Assign one role to one member. Idempotent on Discord's side — re-running on a member who already has the role is a 204 no-op.  Path shape mirrors Discord's own API (`PUT /guilds/{guild}/members/{user}/roles/{role}`) for zero-translation mental mapping.  Bot needs MANAGE_ROLES permission in the guild AND its highest role must be above the target role (Discord hierarchy rule). The `@everyone` role (where roleId == guildId) cannot be assigned. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**guild_id** | **String** |  | [required] |
**user_id** | **String** | Discord user snowflake to assign the role to. | [required] |
**role_id** | **String** |  | [required] |
**account_id** | **String** |  | [required] |

### Return type

[**models::AddDiscordMemberRole200Response**](addDiscordMemberRole_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_discord_guild_role

> models::CreateDiscordGuildRole201Response create_discord_guild_role(guild_id, account_id, create_discord_guild_role_request)
Create a Discord guild role

Creates a new role in the guild.  Requires the bot to hold the Manage Roles permission. Guilds that added the Zernio bot before role management shipped must re-invite it, because Discord applies the permission set at invite time.  Discord's role hierarchy applies: the bot cannot create a role positioned at or above its own highest role, and cannot grant permissions it does not itself hold. Either attempt returns a 403 carrying Discord's own error. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**guild_id** | **String** | Discord guild snowflake ID | [required] |
**account_id** | **String** | SocialAccount _id of the Discord account bound to this guild | [required] |
**create_discord_guild_role_request** | [**CreateDiscordGuildRoleRequest**](CreateDiscordGuildRoleRequest.md) |  | [required] |

### Return type

[**models::CreateDiscordGuildRole201Response**](createDiscordGuildRole_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_discord_scheduled_event

> models::CreateDiscordScheduledEvent200Response create_discord_scheduled_event(guild_id, create_discord_scheduled_event_request)
Create a Discord scheduled event

Create a guild scheduled event. Three event types, selected via the discriminator on `entity.type`:    - `external` — off-platform (Zoom, in-person, livestream). Requires     both `location` and `endsAt`. Most common type for scheduler     integrations.   - `voice` — hosted in a Discord voice channel. Requires `channelId`.   - `stage` — hosted in a Discord stage channel. Requires `channelId`.  Bot needs MANAGE_EVENTS in the guild. Existing installs (pre-events PR) need a re-invite OR a server admin manually granting the permission — see route header for details. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**guild_id** | **String** |  | [required] |
**create_discord_scheduled_event_request** | [**CreateDiscordScheduledEventRequest**](CreateDiscordScheduledEventRequest.md) |  | [required] |

### Return type

[**models::CreateDiscordScheduledEvent200Response**](createDiscordScheduledEvent_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_discord_thread

> models::CreateDiscordThread200Response create_discord_thread(channel_id, account_id, create_discord_thread_request)
Create a Discord public thread

Creates a public thread in a channel. Pass `messageId` to start the thread from an existing message, or omit it to create a standalone thread.  Threads created here are always public. Requires the bot to hold Create Public Threads, which the Zernio bot requests at install time. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**channel_id** | **String** | Discord channel snowflake ID | [required] |
**account_id** | **String** | SocialAccount _id of the Discord account bound to this channel's guild | [required] |
**create_discord_thread_request** | [**CreateDiscordThreadRequest**](CreateDiscordThreadRequest.md) |  | [required] |

### Return type

[**models::CreateDiscordThread200Response**](createDiscordThread_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## crosspost_discord_message

> models::CrosspostDiscordMessage200Response crosspost_discord_message(channel_id, message_id, account_id)
Crosspost Discord message

Publishes a message from an announcement channel so it propagates to every server following that channel.  The source channel must be an announcement channel. Calling this on a regular text channel returns a 400 before Discord is contacted, because Discord's own error for this case is opaque. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**channel_id** | **String** | Discord announcement channel snowflake ID | [required] |
**message_id** | **String** | Discord message snowflake ID | [required] |
**account_id** | **String** | SocialAccount _id of the Discord account bound to this channel's guild | [required] |

### Return type

[**models::CrosspostDiscordMessage200Response**](crosspostDiscordMessage_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_discord_guild_role

> models::UpdateYoutubeDefaultPlaylist200Response delete_discord_guild_role(guild_id, role_id, account_id)
Delete a Discord guild role

Permanently deletes a role from the guild and removes it from every member. This cannot be undone.  Requires the bot to hold Manage Roles, and the target role must sit below the bot's highest role. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**guild_id** | **String** | Discord guild snowflake ID | [required] |
**role_id** | **String** | Discord role snowflake ID | [required] |
**account_id** | **String** | SocialAccount _id of the Discord account bound to this guild | [required] |

### Return type

[**models::UpdateYoutubeDefaultPlaylist200Response**](updateYoutubeDefaultPlaylist_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_discord_message

> models::UpdateYoutubeDefaultPlaylist200Response delete_discord_message(channel_id, message_id, account_id)
Delete a Discord channel message

Deletes a message from a channel, for moderation and cleanup. This cannot be undone.  Deleting a message the bot did not send requires the bot to hold the Manage Messages permission, which the Zernio bot requests at install time. Deleting the bot's own message needs no extra permission.  Ownership is verified by resolving the channel's guild and confirming the caller owns a Discord account bound to it. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**channel_id** | **String** | Discord channel snowflake ID | [required] |
**message_id** | **String** | Discord message snowflake ID | [required] |
**account_id** | **String** | SocialAccount _id of the Discord account bound to this channel's guild | [required] |

### Return type

[**models::UpdateYoutubeDefaultPlaylist200Response**](updateYoutubeDefaultPlaylist_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_discord_scheduled_event

> models::DeleteDiscordScheduledEvent200Response delete_discord_scheduled_event(guild_id, event_id, account_id)
Delete a Discord scheduled event

Hard-delete an event. Use PATCH with `status: 'cancelled'` instead if you want the event preserved in the guild's history. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**guild_id** | **String** |  | [required] |
**event_id** | **String** |  | [required] |
**account_id** | **String** |  | [required] |

### Return type

[**models::DeleteDiscordScheduledEvent200Response**](deleteDiscordScheduledEvent_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## edit_discord_guild_role

> models::CreateDiscordGuildRole201Response edit_discord_guild_role(guild_id, role_id, account_id, edit_discord_guild_role_request)
Edit a Discord guild role

Updates a role's name, color, hoist, mentionable flag, or permission bitfield. At least one field must be supplied. Omitted fields are left unchanged.  Requires the bot to hold Manage Roles, and the target role must sit below the bot's highest role. See the create-role operation for the re-invite requirement. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**guild_id** | **String** | Discord guild snowflake ID | [required] |
**role_id** | **String** | Discord role snowflake ID | [required] |
**account_id** | **String** | SocialAccount _id of the Discord account bound to this guild | [required] |
**edit_discord_guild_role_request** | [**EditDiscordGuildRoleRequest**](EditDiscordGuildRoleRequest.md) |  | [required] |

### Return type

[**models::CreateDiscordGuildRole201Response**](createDiscordGuildRole_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


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


## get_discord_guild_member

> models::GetDiscordGuildMember200Response get_discord_guild_member(guild_id, user_id, account_id)
Get a Discord guild member

Fetch a single guild member by Discord user id.  Does not require the privileged Server Members Intent, so this works even where the full member listing returns 403. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**guild_id** | **String** |  | [required] |
**user_id** | **String** | Discord user snowflake. | [required] |
**account_id** | **String** |  | [required] |

### Return type

[**models::GetDiscordGuildMember200Response**](getDiscordGuildMember_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_discord_scheduled_event

> models::CreateDiscordScheduledEvent200Response get_discord_scheduled_event(guild_id, event_id, account_id)
Get a Discord scheduled event

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**guild_id** | **String** |  | [required] |
**event_id** | **String** |  | [required] |
**account_id** | **String** |  | [required] |

### Return type

[**models::CreateDiscordScheduledEvent200Response**](createDiscordScheduledEvent_200_response.md)

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


## list_discord_guild_members

> models::ListDiscordGuildMembers200Response list_discord_guild_members(guild_id, account_id, limit, after)
List Discord guild members

Cursor-paginated list of guild members. Returns Discord's raw member objects so callers can build community-ops automation (e.g. \"add role to all members joined in the last 7 days\") on the actual platform shape.  **Important:** this endpoint requires the privileged \"Server Members Intent\" on the Discord application. If the intent is not enabled, Discord rejects the call and this endpoint returns **403**. Single member lookup and prefix search (see the sibling endpoints) do not need the intent.  Pagination: pass `after` = the last `user.id` from the previous page. Omit on the first call. Response includes a `nextCursor` and `hasMore` flag so callers don't need to know Discord's pagination shape. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**guild_id** | **String** |  | [required] |
**account_id** | **String** |  | [required] |
**limit** | Option<**i32**> | Page size (1-1000). |  |[default to 100]
**after** | Option<**String**> | Snowflake of the last member from the previous page. |  |

### Return type

[**models::ListDiscordGuildMembers200Response**](listDiscordGuildMembers_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_discord_guild_roles

> models::ListDiscordGuildRoles200Response list_discord_guild_roles(guild_id, account_id)
List Discord guild roles

Returns all roles in a Discord guild. Useful for building role-mention pickers, role-permission UIs, or finding the role ID before calling the role-assign endpoint.  Roles are returned unordered — sort client-side by `position` if you need Discord's UI ordering.  Caller must pass `accountId` of a Discord SocialAccount bound to this guild (route verifies team access + guild match). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**guild_id** | **String** | Discord guild snowflake ID | [required] |
**account_id** | **String** | SocialAccount _id of the Discord account bound to this guild | [required] |

### Return type

[**models::ListDiscordGuildRoles200Response**](listDiscordGuildRoles_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_discord_pinned_messages

> models::ListDiscordPinnedMessages200Response list_discord_pinned_messages(channel_id, account_id)
List pinned messages

Returns the channel's pinned messages, sorted most-recently-pinned first. Discord caps a channel at 50 pinned messages and returns the full list unpaginated.  Bot needs READ_MESSAGE_HISTORY in the channel (granted by default BOT_PERMISSIONS). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**channel_id** | **String** | Discord channel snowflake. | [required] |
**account_id** | **String** | SocialAccount _id of any Discord account in the same guild. | [required] |

### Return type

[**models::ListDiscordPinnedMessages200Response**](listDiscordPinnedMessages_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_discord_scheduled_events

> models::ListDiscordScheduledEvents200Response list_discord_scheduled_events(guild_id, account_id, with_user_count)
List Discord scheduled events

Return all scheduled events in the guild. Events are distinct from messages — they appear in the server's Events panel and Discord auto-notifies interested members ahead of start time.  Pass `withUserCount=true` to include `user_count` (number of members who RSVP'd) on each event. Useful for surfacing engagement. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**guild_id** | **String** |  | [required] |
**account_id** | **String** |  | [required] |
**with_user_count** | Option<**bool**> | Include user_count on each event. |  |

### Return type

[**models::ListDiscordScheduledEvents200Response**](listDiscordScheduledEvents_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## pin_discord_message

> models::PinDiscordMessage200Response pin_discord_message(channel_id, message_id, account_id)
Pin a Discord message

Pin a specific message in a channel. Path shape mirrors Discord's own API (`PUT /channels/{cid}/pins/{mid}`).  Idempotent — re-pinning an already-pinned message is a 204 no-op.  Constraints:   - Bot needs MANAGE_MESSAGES in the channel.   - 50-pin cap per channel — hitting it returns 400 (Discord-side).     Caller should unpin one first. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**channel_id** | **String** |  | [required] |
**message_id** | **String** |  | [required] |
**account_id** | **String** |  | [required] |

### Return type

[**models::PinDiscordMessage200Response**](pinDiscordMessage_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_discord_member_role

> models::RemoveDiscordMemberRole200Response remove_discord_member_role(guild_id, user_id, role_id, account_id)
Remove a role from a guild member

Remove one role from one member. Idempotent — removing a role the member doesn't have returns 204 no-op.  Same permission + hierarchy constraints as the PUT counterpart. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**guild_id** | **String** |  | [required] |
**user_id** | **String** |  | [required] |
**role_id** | **String** |  | [required] |
**account_id** | **String** |  | [required] |

### Return type

[**models::RemoveDiscordMemberRole200Response**](removeDiscordMemberRole_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## search_discord_guild_members

> models::SearchDiscordGuildMembers200Response search_discord_guild_members(guild_id, account_id, query, limit)
Search Discord guild members

Search guild members whose username or nickname **starts with** the query (Discord matches prefixes only, not substrings).  Does not require the privileged Server Members Intent, so this works even where the full member listing returns 403. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**guild_id** | **String** |  | [required] |
**account_id** | **String** |  | [required] |
**query** | **String** | Username or nickname prefix to match. | [required] |
**limit** | Option<**i32**> |  |  |[default to 25]

### Return type

[**models::SearchDiscordGuildMembers200Response**](searchDiscordGuildMembers_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## send_discord_direct_message

> models::SendDiscordDirectMessage200Response send_discord_direct_message(send_discord_direct_message_request)
Send a Discord Direct Message

Send a 1:1 Direct Message from the bot to a Discord user (by snowflake ID). Supports the same payload shape as channel posts — content, embeds, media attachments, and TTS.  Constraints (Discord platform limits):   - The bot can only DM users it shares at least one guild with.   - If the recipient has DMs disabled for non-friends, Discord returns 403     (surfaces as a 502 platform error).   - `content` capped at 2,000 chars.   - At least one of `content`, `embeds`, or `attachments` is required.   - The recipient must be identified by Discord snowflake ID (not username).  This is a dedicated endpoint rather than a `POST /v1/posts` variant because DMs are 1:1 operational messages (onboarding, billing reminders, support pings) with a different lifecycle than scheduled channel posts. DMs are not persisted to `Post` / `ExternalPost` and are always sent immediately. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**send_discord_direct_message_request** | [**SendDiscordDirectMessageRequest**](SendDiscordDirectMessageRequest.md) |  | [required] |

### Return type

[**models::SendDiscordDirectMessage200Response**](sendDiscordDirectMessage_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## unpin_discord_message

> models::UnpinDiscordMessage200Response unpin_discord_message(channel_id, message_id, account_id)
Unpin a Discord message

Unpin a message. Same MANAGE_MESSAGES permission requirement as pin. Idempotent — unpinning a non-pinned message is a 204 no-op. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**channel_id** | **String** |  | [required] |
**message_id** | **String** |  | [required] |
**account_id** | **String** |  | [required] |

### Return type

[**models::UnpinDiscordMessage200Response**](unpinDiscordMessage_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_discord_scheduled_event

> models::CreateDiscordScheduledEvent200Response update_discord_scheduled_event(guild_id, event_id, update_discord_scheduled_event_request)
Update a Discord scheduled event

Patch any subset of fields. Passing `status: 'cancelled'` is how you cancel an event — Discord doesn't have a dedicated cancel endpoint, it's a status transition.  Most status transitions Discord enforces (you can't go SCHEDULED → COMPLETED directly). The common consumer case is SCHEDULED → CANCELED. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**guild_id** | **String** |  | [required] |
**event_id** | **String** |  | [required] |
**update_discord_scheduled_event_request** | [**UpdateDiscordScheduledEventRequest**](UpdateDiscordScheduledEventRequest.md) |  | [required] |

### Return type

[**models::CreateDiscordScheduledEvent200Response**](createDiscordScheduledEvent_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
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

