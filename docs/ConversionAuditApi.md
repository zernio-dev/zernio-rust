# \ConversionAuditApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**audit_conversion_tracking**](ConversionAuditApi.md#audit_conversion_tracking) | **GET** /v1/conversion-audit | Audit a site's ad conversion tracking
[**create_conversion_audit_monitor**](ConversionAuditApi.md#create_conversion_audit_monitor) | **POST** /v1/conversion-audit/monitors | Watch a domain
[**delete_conversion_audit_monitor**](ConversionAuditApi.md#delete_conversion_audit_monitor) | **DELETE** /v1/conversion-audit/monitors/{monitorId} | Stop watching a domain
[**get_latest_conversion_audit**](ConversionAuditApi.md#get_latest_conversion_audit) | **GET** /v1/conversion-audit/latest | Get a host's latest stored conversion audit
[**get_meta_conversion_audit**](ConversionAuditApi.md#get_meta_conversion_audit) | **GET** /v1/conversion-audit/meta-audit | Audit a connected Meta pixel from inside Events Manager
[**list_conversion_audit_monitors**](ConversionAuditApi.md#list_conversion_audit_monitors) | **GET** /v1/conversion-audit/monitors | List watched domains



## audit_conversion_tracking

> models::ConversionAuditAnswer audit_conversion_tracking(url)
Audit a site's ad conversion tracking

Scan any public URL for ad-platform conversion tracking, score how much conversion signal it leaks before the ad platforms see it, and get a fix prompt to hand to a coding agent.  The API key is optional. Without one, a caller's IP address gets 20 scans a minute. The Zernio MCP server always needs a key, because its sign-in covers the whole connection.  The scan fetches the page (SSRF-guarded) and its Google Tag Manager containers, and can render it in a headless browser. It finds every ad platform's browser pixel, checks for visible server-side (Conversions API) tracking, and estimates the signal lost to ad blockers, browser limits and short cookie windows.  Visitors who decline consent are never counted as lost.  The scan reads the page only and changes nothing on the site. Like the free page, it publishes the result as the host's public report.  Reading the result:  - `report.visibility: \"limited\"` means some pixels load through a tag manager or a store platform, so only part of the setup is visible from outside. It does not mean the tracking failed or is missing. - `status: \"warn\"` (browser-only) is the leak: the platform is tracked in the browser but not server-side. - `status: \"good\"` (server-side) means conversions reach the platform server-side, which recovers most of that signal. - `fixPrompt` is the same fix prompt the Conversion Leak Report page shows: this scan's findings, then the steps to send conversions server-side with `POST /v1/events` and to verify them. - To fix the leak with Zernio, follow https://docs.zernio.com/products/server-side-tracking/fix-with-agent: a tracking site, its tag, a forwarding rule per network to the pixel the page runs, then a rescan. A network turns `good` once the site's events reached that pixel in the last 7 days. - `publicReport` links the host's public page on is-bleeding.com. A homepage scan that could read the site's pixels becomes that page's snapshot, the same as a scan on is-bleeding.com. Any other scan links the stored snapshot, taken at `scannedAt`, or returns null when the host has none.  Without a key, each IP address also shares one hourly ceiling with every other keyless caller. With a key, a user gets 60 scans a minute. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**url** | **String** | The website address to audit. A bare domain is accepted and normalized to https. | [required] |

### Return type

[**models::ConversionAuditAnswer**](ConversionAuditAnswer.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_conversion_audit_monitor

> models::ConversionAuditMonitorAnswer create_conversion_audit_monitor(create_conversion_audit_monitor_request)
Watch a domain

Watch a domain's conversion tracking. Zernio rescans its homepage once a day and emails the account's address when tracking breaks, with what changed and the fix prompt for a coding agent. A break is:  - a score drop of 5 points or more - an ad network that stops tracking or stops firing - a pixel that starts firing before the cookie banner is answered - a server-side path that disappears  A break is confirmed by a second scan before any email goes out. The first check compares against the host's stored report when it has one, so run `auditConversionTracking` first to start from today's state.  Watching a domain you already watch returns it with `created: false` and status `200`. An account can watch up to 25 domains. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_conversion_audit_monitor_request** | [**CreateConversionAuditMonitorRequest**](CreateConversionAuditMonitorRequest.md) |  | [required] |

### Return type

[**models::ConversionAuditMonitorAnswer**](ConversionAuditMonitorAnswer.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_conversion_audit_monitor

> models::DeleteAutomationTemplate200Response delete_conversion_audit_monitor(monitor_id)
Stop watching a domain

Stops the daily checks and alert emails for this domain. The host's public report stays.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**monitor_id** | **String** | The monitor's `id`, from `listConversionAuditMonitors` or `createConversionAuditMonitor`. | [required] |

### Return type

[**models::DeleteAutomationTemplate200Response**](deleteAutomationTemplate_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_latest_conversion_audit

> models::GetLatestConversionAudit200Response get_latest_conversion_audit(host)
Get a host's latest stored conversion audit

Read the latest stored Conversion Leak Report for a host without running a new scan. Each homepage scan on is-bleeding.com that could read the site's pixels replaces that host's stored report. Scans made with `auditConversionTracking` are stored the same way.  The API key is optional. Without one, a caller's IP address gets 60 requests a minute. The Zernio MCP server always needs a key.  Returns `404` when the host has no stored report. Run `auditConversionTracking` to scan it now. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**host** | **String** | The host to look up. A full URL is reduced to its host; `www.` and letter case are ignored. | [required] |

### Return type

[**models::GetLatestConversionAudit200Response**](getLatestConversionAudit_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_meta_conversion_audit

> models::MetaDatasetAudit get_meta_conversion_audit(account_id, ad_account_id, pixel_id)
Audit a connected Meta pixel from inside Events Manager

The connected follow-up to the Conversion Leak Report. A page scan only sees the browser; this reads what Meta itself recorded for the ad account's pixel (dataset) with the connection's own token, over the last 7 days.  ### What it reads  - each event's volume per day, its last 24 hours and the last hour Meta counted it in - the share of each event that arrived through the Conversions API (server) rather than the browser pixel - Event Match Quality per event, with the coverage of every customer-information key Meta matched on (email, phone, external id, IP address, user agent, `fbp`, `fbc`, name and address fields) - the event_id, external_id and fbp deduplication coverage of browser and server copies, where an event has both - Meta's diagnostics for the dataset and its failed dataset checks - whether automatic advanced matching and first-party cookies are on  Each `findings` entry is a problem one of those numbers shows, with its fix and who makes it (`fix.by`):  - `zernio`: turning on Zernio server-side events or the Zernio site tag fixes it - `you`: a change in your site or API call - `meta`: a setting only Events Manager has  Meta does not return a business's verified domains or an Aggregated Event Measurement setup to this API, so both are listed under `unavailable`, with any read Meta refused.  `accountId` is a Meta ads connection (or the Facebook account it belongs to). Without `adAccountId`, the first selected ad account that has a pixel is audited; without `pixelId`, its most recently active pixel. The result is cached for 10 minutes per pixel. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Meta ads connection to read with. | [required] |
**ad_account_id** | Option<**String**> | The ad account whose pixel is audited. Must be selected on the connection. |  |
**pixel_id** | Option<**String**> | One of the ad account's pixels (`datasets[].id`). |  |

### Return type

[**models::MetaDatasetAudit**](MetaDatasetAudit.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_conversion_audit_monitors

> models::ListConversionAuditMonitors200Response list_conversion_audit_monitors()
List watched domains

The domains you watch with the Conversion Leak Report, each with its last score and the score of each daily check.  Zernio rescans every watched domain once a day. When tracking breaks, it emails you what changed and the fix prompt. `createConversionAuditMonitor` lists what counts as a break. 

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::ListConversionAuditMonitors200Response**](listConversionAuditMonitors_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

