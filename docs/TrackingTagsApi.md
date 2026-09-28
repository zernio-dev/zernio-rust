# \TrackingTagsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_tracking_tag_shared_account**](TrackingTagsApi.md#add_tracking_tag_shared_account) | **POST** /v1/accounts/{accountId}/tracking-tags/{tagId}/shared-accounts | Share with an ad account
[**create_tracking_tag**](TrackingTagsApi.md#create_tracking_tag) | **POST** /v1/accounts/{accountId}/tracking-tags | Create a tracking tag
[**create_tracking_tag_event**](TrackingTagsApi.md#create_tracking_tag_event) | **POST** /v1/accounts/{accountId}/tracking-tags/{tagId}/events | Create a conversion event
[**delete_tracking_tag_event**](TrackingTagsApi.md#delete_tracking_tag_event) | **DELETE** /v1/accounts/{accountId}/tracking-tags/{tagId}/events/{eventId} | Delete a conversion event
[**get_ad_tracking_tags**](TrackingTagsApi.md#get_ad_tracking_tags) | **GET** /v1/ads/{adId}/tracking-tags | Get ad tracking tags
[**get_tracking_tag**](TrackingTagsApi.md#get_tracking_tag) | **GET** /v1/accounts/{accountId}/tracking-tags/{tagId} | Get a tracking tag
[**get_tracking_tag_stats**](TrackingTagsApi.md#get_tracking_tag_stats) | **GET** /v1/accounts/{accountId}/tracking-tags/{tagId}/stats | Get aggregated event stats
[**get_tracking_tag_store_install**](TrackingTagsApi.md#get_tracking_tag_store_install) | **GET** /v1/accounts/{accountId}/tracking-tags/{tagId}/install | Get store install status
[**install_tracking_tag_on_store**](TrackingTagsApi.md#install_tracking_tag_on_store) | **POST** /v1/accounts/{accountId}/tracking-tags/{tagId}/install | Install on a Shopify store or WordPress site
[**list_tracking_tag_events**](TrackingTagsApi.md#list_tracking_tag_events) | **GET** /v1/accounts/{accountId}/tracking-tags/{tagId}/events | List conversion events
[**list_tracking_tag_shared_accounts**](TrackingTagsApi.md#list_tracking_tag_shared_accounts) | **GET** /v1/accounts/{accountId}/tracking-tags/{tagId}/shared-accounts | List accounts it is shared with
[**list_tracking_tags**](TrackingTagsApi.md#list_tracking_tags) | **GET** /v1/accounts/{accountId}/tracking-tags | List tracking tags
[**remove_tracking_tag_from_store**](TrackingTagsApi.md#remove_tracking_tag_from_store) | **DELETE** /v1/accounts/{accountId}/tracking-tags/{tagId}/install | Remove from a Shopify store or WordPress site
[**remove_tracking_tag_shared_account**](TrackingTagsApi.md#remove_tracking_tag_shared_account) | **DELETE** /v1/accounts/{accountId}/tracking-tags/{tagId}/shared-accounts | Stop sharing with an account
[**update_ad_tracking_tags**](TrackingTagsApi.md#update_ad_tracking_tags) | **PATCH** /v1/ads/{adId}/tracking-tags | Set ad tracking tags
[**update_tracking_tag**](TrackingTagsApi.md#update_tracking_tag) | **PATCH** /v1/accounts/{accountId}/tracking-tags/{tagId} | Update a tracking tag
[**update_tracking_tag_event**](TrackingTagsApi.md#update_tracking_tag_event) | **PATCH** /v1/accounts/{accountId}/tracking-tags/{tagId}/events/{eventId} | Update a conversion event



## add_tracking_tag_shared_account

> models::AddTrackingTagSharedAccount201Response add_tracking_tag_shared_account(account_id, tag_id, add_tracking_tag_shared_account_request)
Share with an ad account

Shares the pixel with another ad account so campaigns/audiences in that account can use it. Requires that you administer both the pixel's owning Business Manager and the target ad account; a pixel on a personal (non-BM) ad account can't be shared (Meta will reject the call). Meta only (platform `metaads`); other platforms return 501. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**tag_id** | **String** | Pixel id. | [required] |
**add_tracking_tag_shared_account_request** | [**AddTrackingTagSharedAccountRequest**](AddTrackingTagSharedAccountRequest.md) |  | [required] |

### Return type

[**models::AddTrackingTagSharedAccount201Response**](addTrackingTagSharedAccount_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_tracking_tag

> models::CreateTrackingTag201Response create_tracking_tag(account_id, create_tracking_tag_request)
Create a tracking tag

Meta: creates a Meta Pixel on the given ad account (`POST /act_{id}/adspixels`, where `name` is the only input). Returns the created tag including its install `code`. The pixel is owned by the Business Manager that owns the ad account; a pixel created on a personal (non-BM) ad account ends up with `ownerBusinessId: null` and can't be shared with other ad accounts.  Creating a Meta pixel does NOT install it. Install the returned `code` snippet on the site, or send events server-side via `POST /v1/ads/conversions`. The check `installed` is derived from `lastFiredTime`.  OpenAI Ads: creates an OpenAI pixel AND provisions a Conversions API key for it in the same call (`adAccountId` is required by this endpoint but ignored: one API key maps to exactly one ad account, so there's nothing to select). Returns 422 (`FEATURE_NOT_AVAILABLE`) if the ad account isn't enabled for pixel management; contact your OpenAI partner representative to enable it. There is no delete API for OpenAI pixels. If the pixel is created but the Conversions API key provisioning then fails, the pixel is left live on OpenAI (it cannot be cleaned up) and the error message names the surviving pixel id and warns against retrying, since a retry would create a second, orphaned pixel.  NOT idempotent on either platform: each call creates a new pixel (and, for OpenAI, a new Conversions API key plus, with `defaultEventType`, a new conversion event setting). Do not retry blindly on timeout. Meta (platform `metaads`) and OpenAI Ads (platform `openaiads`); other platforms return 501. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Ads SocialAccount id (platform `metaads` or `openaiads`). | [required] |
**create_tracking_tag_request** | [**CreateTrackingTagRequest**](CreateTrackingTagRequest.md) |  | [required] |

### Return type

[**models::CreateTrackingTag201Response**](createTrackingTag_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_tracking_tag_event

> models::CreateTrackingTagEvent201Response create_tracking_tag_event(account_id, tag_id, create_tracking_tag_event_request)
Create a conversion event

Creates a conversion event tied to the tag. Pass the platform's own event type in `type` (e.g. Google `PURCHASE`, LinkedIn `ADD_TO_CART`, X `CHECKOUT_INITIATED`) or a neutral `siteEvent` the platform maps to its closest type. Each platform stores a subset of the optional fields; sending one it does not store answers 400 naming the supported fields. NOT idempotent unless noted per platform: do not retry blindly.  OpenAI Ads: creates a conversion event setting on the pixel (`POST /conversions/event_settings`, source = the pixel). Accepts `name`, `type` and `siteEvent` only. `type` is a standard event (`order_created`, `lead_created`, `items_added`, `contents_viewed`, `checkout_started`, `registration_completed`, `subscription_created`, `trial_started`, `appointment_scheduled`, `page_viewed`, `app_installed`, `app_opened`) or, for anything else, the custom event name itself (1 to 64 letters, digits, underscores or dashes; stored lowercase). `siteEvent` maps `search` and `add_payment_info` to the custom events `search` and `addpaymentinfo`, the names Zernio's Shopify pixel sends. The click attribution window is 30 days, the only value OpenAI documents. Only standard events can be a conversions campaign's optimization goal. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**tag_id** | **String** | Tag id (`TrackingTag.id`). | [required] |
**create_tracking_tag_event_request** | [**CreateTrackingTagEventRequest**](CreateTrackingTagEventRequest.md) |  | [required] |

### Return type

[**models::CreateTrackingTagEvent201Response**](createTrackingTagEvent_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_tracking_tag_event

> models::DeleteTrackingTagEvent200Response delete_tracking_tag_event(account_id, tag_id, event_id, ad_account_id)
Delete a conversion event

Removes the conversion event. Platforms without a hard delete archive or disable it instead; `state` in the response says which (`deleted`, `archived`, `disabled`).  OpenAI Ads answers 501: there is no delete or archive route for event settings (`DELETE /v1/conversions/event_settings/{id}` and `POST .../{id}/archive` answer 404 \"Invalid URL\"). Archive the event in OpenAI Ads Manager. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**tag_id** | **String** |  | [required] |
**event_id** | **String** | Event id (`TrackingTagEvent.id`). | [required] |
**ad_account_id** | Option<**String**> | Scopes the lookup on platforms whose tag ids live inside an ad account. |  |

### Return type

[**models::DeleteTrackingTagEvent200Response**](deleteTrackingTagEvent_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad_tracking_tags

> models::GetAdTrackingTags200Response get_ad_tracking_tags(ad_id)
Get ad tracking tags

Unified read of the platform's native click-URL tracking params. - Meta (facebook/instagram): the creative's `url_tags` (and template_url_spec). - Google (googleads): the campaign's `trackingUrlTemplate` + `finalUrlSuffix`. - LinkedIn (linkedinads): the campaign's Dynamic UTM `dynamicValueParameters` + `customValueParameters`. Returns 405 for platforms without a click-URL tracking surface (TikTok, X, Pinterest).  **Not pixels.** Despite the shared path segment, this endpoint has nothing to do with measurement tags. For an ad account's pixels use `GET /v1/accounts/{accountId}/tracking-tags?adAccountId=act_...` (Meta Pixels, with `kind` and `ownerAdAccountId`) or `GET /v1/accounts/{accountId}/conversion-destinations`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_id** | **String** | Ad id (hex _id, platformAdId, or effective story/media id). | [required] |

### Return type

[**models::GetAdTrackingTags200Response**](getAdTrackingTags_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_tracking_tag

> models::GetTrackingTag200Response get_tracking_tag(account_id, tag_id, ad_account_id)
Get a tracking tag

Returns the full tag record including the base-code `code` snippet, `lastFiredTime`, `ownerBusinessId`, `isUnavailable`, etc. Meta only (platform `metaads`); other platforms return 501.  OpenAI Ads (`openaiads`): `tagId` is the pixel's API id (`cds_...`) or its `pixel_id`. OpenAI documents no single-pixel read, so the tag is resolved from the pixel list; the response adds `code` (the official `oaiq` base code plus `page_viewed`) and `events` (the conversion event settings whose source is this pixel). `siteTagId` is the `pixel_id` the site and the Conversions API send; `id` is what event settings reference. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**tag_id** | **String** | Tag id (`TrackingTag.id`). | [required] |
**ad_account_id** | Option<**String**> | Scopes the lookup on platforms whose tag ids live inside an ad account. Ignored elsewhere. |  |

### Return type

[**models::GetTrackingTag200Response**](getTrackingTag_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_tracking_tag_stats

> models::GetTrackingTagStats200Response get_tracking_tag_stats(account_id, tag_id, ad_account_id, aggregation, start_time, end_time)
Get aggregated event stats

Returns event counts / health for the tag, where the platform exposes them. Meta: aggregated counts (`GET /{pixel_id}/stats`), rows passed through as-is; their shape depends on the `aggregation` requested. Platforms without a stats API answer 501.  OpenAI Ads: the recent-events stream (`GET /conversions/events`), the latest (at most 50) Pixel SDK events received in the last 15 minutes, one row per event (`event_type`, `api_channel`, `event_timestamp_ms`, `received_at_ms`, ...). Conversions API events are not included. It is a fixed window: `startTime`/`endTime` answer 400. Use it to confirm an install fires; attributed totals come from ads analytics. Accounts not enabled for the stream answer 422 `feature_not_available`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**tag_id** | **String** | Tag id (`TrackingTag.id`). | [required] |
**ad_account_id** | Option<**String**> | Scopes the lookup on platforms whose tag ids live inside an ad account. Ignored elsewhere. |  |
**aggregation** | Option<**String**> | Meta only (400 on other platforms): aggregation dimension. Defaults to `event`. |  |[default to event]
**start_time** | Option<**i32**> | Unix seconds lower bound. |  |
**end_time** | Option<**i32**> | Unix seconds upper bound. |  |

### Return type

[**models::GetTrackingTagStats200Response**](getTrackingTagStats_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_tracking_tag_store_install

> models::GetTrackingTagStoreInstall200Response get_tracking_tag_store_install(account_id, tag_id, store_account_id, ad_account_id)
Get store install status

Whether this tag is the one the Shopify store fires for its platform. `installedTagId` names the tag of that platform the store currently fires, which can be a different tag, and `tags` lists every Zernio tag on the store (all platforms).  WordPress: whether the Zernio widget for this pixel is live (in an active widget area, script intact), plus a read-only `preflight` with the theme's widget areas and, when an install would be blocked, the `reason` POST would return. The preflight reads capabilities only, so `ready: true` is not a guarantee: `DISALLOW_UNFILTERED_HTML` or a multisite admin who is not a Super Admin still strips the script, which POST detects. `tags` lists every Zernio widget on the site (all platforms, with `active`). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**tag_id** | **String** | Tag id (`TrackingTag.id`). | [required] |
**store_account_id** | **String** | The connected Shopify or WordPress account id. | [required] |
**ad_account_id** | Option<**String**> | Scopes the tag lookup on platforms whose tag ids live inside an ad account. |  |

### Return type

[**models::GetTrackingTagStoreInstall200Response**](getTrackingTagStoreInstall_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## install_tracking_tag_on_store

> models::InstallTrackingTagOnStore200Response install_tracking_tag_on_store(account_id, tag_id, install_tracking_tag_on_store_request)
Install on a Shopify store or WordPress site

Puts the Meta pixel on a connected Shopify store's storefront and checkout through Zernio's Shopify web pixel (a Shopify app pixel, no theme edits). The store then sends PageView, ViewContent, AddToCart, Search, InitiateCheckout, AddPaymentInfo and Purchase (with value, currency, content_ids and contents) to the pixel, each with an event id. Purchase uses `shopify_order_{orderId}` as its event id, so a Conversions API Purchase you send for the same order with that `eventId` is deduplicated by Meta.  Idempotent: a store runs one Zernio web pixel holding one tag per platform, so calling it again updates the install, installing a different tag of the same platform replaces the previous one (reported in `replacedTagId`), and other platforms' tags are kept. Events respect the store's customer privacy settings (marketing consent).  `accountId` is the Meta ads account that owns the pixel (`tagId`); `storeAccountId` is the Shopify account.  OpenAI Ads on Shopify: each event is sent through OpenAI's documented image tag (`GET https://bzr.openai.com/v1/sdk/events`) as `page_viewed`, `contents_viewed`, `items_added`, `checkout_started`, `order_created`, and custom events `search` and `addpaymentinfo` (lowercase, so a Conversions API Search/AddPaymentInfo with the same event id deduplicates). Amounts are sent in the currency's minor unit. The landing page's `oppref` click id is kept in the `__oppref` cookie for 30 days and sent with every event. The image tag cannot carry the `__obref` browser id (OpenAI rejects the parameter), and the search text is never sent. On WordPress the widget holds the official `oaiq` base code and a `page_viewed` call.  Stores connected before pixel support must re-approve the Zernio app: the call then answers 409 `reconnect_required` with `details.authUrl` to send the merchant to (the Shopify account id stays the same). Platforms without an install path return 501.  **WordPress** (`storeAccountId` is a connected WordPress.com or self-hosted site): Zernio adds a Custom HTML widget with the Meta pixel base code (fbevents.js, `init`, `PageView`) to a widget area of the active theme (a footer area when there is one, else the first active area; pass `sidebarId` to choose), then reads the widget back to confirm WordPress kept the `<script>` tag. The widget carries a Zernio marker, so the call is idempotent per pixel: repeating it updates or moves the same widget, and pixel code the site owner pasted by hand is never touched. Several pixels can run side by side (one widget each). When the site cannot run the pixel, nothing is left behind and the call answers 422 `tracking_tag_install_blocked` with `details.reason`: - `insufficient_permissions`: the connected user lacks `edit_theme_options` (needs Administrator). - `scripts_stripped`: WordPress removed the script (the user lacks `unfiltered_html`, e.g. a multisite admin who is not a Super Admin, or `DISALLOW_UNFILTERED_HTML` is set). - `wordpress_com_plan`: a WordPress.com plan that strips scripts (plans without plugins). - `no_widget_areas`: the theme has no widget areas (block themes such as Twenty Twenty-Five). - `widgets_api_unavailable`: no widgets REST API (WordPress older than 5.8, or disabled). The `error` message names the manual alternative (Meta's official WordPress plugin). With `verifyHomepage` (default true) the homepage is fetched afterwards and `homepageCheck` says whether the pixel is visible; `not_found` can be a stale page cache, the widget read-back is authoritative. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**tag_id** | **String** | Tag id (`TrackingTag.id`). | [required] |
**install_tracking_tag_on_store_request** | [**InstallTrackingTagOnStoreRequest**](InstallTrackingTagOnStoreRequest.md) |  | [required] |

### Return type

[**models::InstallTrackingTagOnStore200Response**](installTrackingTagOnStore_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_tracking_tag_events

> models::ListTrackingTagEvents200Response list_tracking_tag_events(account_id, tag_id, ad_account_id)
List conversion events

The tag's conversion events, on platforms where each conversion is its own object: Google conversion actions, LinkedIn conversion rules, X web event tags, OpenAI event settings, TikTok pixel events, Meta custom conversions. Platforms where events are just names the site sends (Pinterest) answer 501.  OpenAI Ads: the account's conversion event settings whose source is this pixel. `siteEventId` is the event name the site sends (a standard event such as `order_created`, or the lowercase custom event name); `clickWindowDays` is the attribution window. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**tag_id** | **String** | Tag id (`TrackingTag.id`). | [required] |
**ad_account_id** | Option<**String**> | Scopes the lookup on platforms whose tag ids live inside an ad account. |  |

### Return type

[**models::ListTrackingTagEvents200Response**](listTrackingTagEvents_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_tracking_tag_shared_accounts

> models::ListTrackingTagSharedAccounts200Response list_tracking_tag_shared_accounts(account_id, tag_id)
List accounts it is shared with

Meta only (platform `metaads`); other platforms return 501.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**tag_id** | **String** | Pixel id. | [required] |

### Return type

[**models::ListTrackingTagSharedAccounts200Response**](listTrackingTagSharedAccounts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_tracking_tags

> models::ListTrackingTags200Response list_tracking_tags(account_id, ad_account_id)
List tracking tags

Returns the tracking tags (Meta Pixels, or OpenAI Ads pixels) the connected ads account can see. Pass `?adAccountId=act_...` (Meta only) to scope the list to a single ad account; omit it to list every pixel reachable by the token (the name is then suffixed with the ad account it was discovered on, for disambiguation). The list view omits `code`. Call `getTrackingTag` for the install snippet and full detail.  Meta (platform `metaads`) and OpenAI Ads (platform `openaiads`); other platforms return 501. The `accountId` must be the ads SocialAccount created by the Ads add-on connect flow (Meta) or the OpenAI Ads connect flow, not a Facebook/Instagram posting account. Get your Meta `act_...` ids from `GET /v1/ads/accounts`; `adAccountId` is ignored for OpenAI Ads (one API key maps to exactly one ad account). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Ads SocialAccount id (platform `metaads` or `openaiads`). | [required] |
**ad_account_id** | Option<**String**> | Optional, Meta only. Scope to one ad account, e.g. `act_123456789`. Ignored for OpenAI Ads. |  |

### Return type

[**models::ListTrackingTags200Response**](listTrackingTags_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_tracking_tag_from_store

> models::RemoveTrackingTagFromStore200Response remove_tracking_tag_from_store(account_id, tag_id, store_account_id, ad_account_id)
Remove from a Shopify store or WordPress site

Removes the tag from the store. Idempotent: nothing installed returns 200 with `installed: false`. If the store fires a different tag of the same platform, nothing is removed and the call answers 409 `invalid_resource_state`. Shopify: other platforms' tags stay; the web pixel itself is deleted once no tag remains.  WordPress: deletes every widget Zernio created for this pixel and reports how many in `removed` (0 when nothing was installed). Pixel code added by hand is left alone. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**tag_id** | **String** | Tag id (`TrackingTag.id`). | [required] |
**store_account_id** | **String** | The connected Shopify or WordPress account id. | [required] |
**ad_account_id** | Option<**String**> | Scopes the tag lookup on platforms whose tag ids live inside an ad account. |  |

### Return type

[**models::RemoveTrackingTagFromStore200Response**](removeTrackingTagFromStore_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_tracking_tag_shared_account

> remove_tracking_tag_shared_account(account_id, tag_id, ad_account_id)
Stop sharing with an account

`adAccountId` may be passed as a query parameter (recommended) or as a JSON body field for clients that can send DELETE bodies. Meta only (platform `metaads`); other platforms return 501. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**tag_id** | **String** | Pixel id. | [required] |
**ad_account_id** | Option<**String**> | Ad account to unshare, e.g. `act_123456789`. May also be sent in the JSON body. |  |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_ad_tracking_tags

> models::UpdateAdTrackingTags200Response update_ad_tracking_tags(ad_id, update_ad_tracking_tags_request)
Set ad tracking tags

Unified update. Send only the fields for the ad's platform: - Meta: `urlTags` (array of {key,value}). Meta creatives are immutable, so this rebuilds the   creative and repoints the ad. By DEFAULT we PRESERVE the existing creative verbatim   (re-post its object_story_spec + the new url_tags, reusing the image), so you send `urlTags`   ALONE, with no need to read back headline/body/CTA. `creative` (headline, body, callToAction,   linkUrl, imageUrl) is OPTIONAL and only needed to rebuild explicitly, or for SHARE / page-post   / dark / asset_feed creatives whose object_story_spec Meta strips (those return 422 asking for   `creative`). - Google: `trackingUrlTemplate` and/or `finalUrlSuffix` (full template strings; account quota applies). - LinkedIn: `dynamicValueParameters` and/or `customValueParameters` (campaign-level Dynamic UTM). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_id** | **String** |  | [required] |
**update_ad_tracking_tags_request** | [**UpdateAdTrackingTagsRequest**](UpdateAdTrackingTagsRequest.md) |  | [required] |

### Return type

[**models::UpdateAdTrackingTags200Response**](updateAdTrackingTags_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_tracking_tag

> models::GetTrackingTag200Response update_tracking_tag(account_id, tag_id, update_tracking_tag_request)
Update a tracking tag

Partial-update a pixel. Whitelisted fields: `name` (rename), `enableAutomaticMatching`, `automaticMatchingFields`, `firstPartyCookieStatus`, `dataUseSetting`. At least one is required. Returns the re-fetched canonical tag. Meta only (platform `metaads`); other platforms return 501.  OpenAI Ads answers 501: its API has no pixel update or delete route (`POST`/`PATCH`/`PUT`/`DELETE /v1/conversions/pixels/{id}` answer 405 \"Invalid method\"); rename a pixel in OpenAI Ads Manager.  There is no DELETE: Meta has no API to delete a pixel. To stop using one, unshare it from your ad accounts (`DELETE .../tracking-tags/{tagId}/shared-accounts`) or disable it in Events Manager. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**tag_id** | **String** | Pixel id. | [required] |
**update_tracking_tag_request** | [**UpdateTrackingTagRequest**](UpdateTrackingTagRequest.md) |  | [required] |

### Return type

[**models::GetTrackingTag200Response**](getTrackingTag_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_tracking_tag_event

> models::CreateTrackingTagEvent201Response update_tracking_tag_event(account_id, tag_id, event_id, tracking_tag_event_input)
Update a conversion event

Partial update; at least one field. A field the platform does not store answers 400.  OpenAI Ads answers 501: OpenAI documents only list and create for event settings, and `POST`/`PATCH`/`PUT /v1/conversions/event_settings/{id}` answer 404 \"Invalid URL\". Create a new event instead. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**tag_id** | **String** |  | [required] |
**event_id** | **String** | Event id (`TrackingTagEvent.id`). | [required] |
**tracking_tag_event_input** | [**TrackingTagEventInput**](TrackingTagEventInput.md) |  | [required] |

### Return type

[**models::CreateTrackingTagEvent201Response**](createTrackingTagEvent_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

