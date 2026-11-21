# \ConversionAuditApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**audit_conversion_tracking**](ConversionAuditApi.md#audit_conversion_tracking) | **GET** /v1/conversion-audit | Audit a site's ad conversion tracking
[**get_latest_conversion_audit**](ConversionAuditApi.md#get_latest_conversion_audit) | **GET** /v1/conversion-audit/latest | Get a host's latest stored conversion audit



## audit_conversion_tracking

> models::ConversionAuditAnswer audit_conversion_tracking(url)
Audit a site's ad conversion tracking

Scan any public URL for ad-platform conversion tracking, score how much conversion signal it leaks before the ad platforms see it, and get a fix prompt to hand to a coding agent.  The API key is optional. Without one, a caller's IP address gets 20 scans a minute. The Zernio MCP server always needs a key, because its sign-in covers the whole connection.  The scan fetches the page (SSRF-guarded) and its Google Tag Manager containers, and can render it in a headless browser. It finds every ad platform's browser pixel, checks for visible server-side (Conversions API) tracking, and estimates the signal lost to iOS/ATT, ad-blockers and short cookie windows.  The scan reads the page only and changes nothing on the site. Like the free page, it publishes the result as the host's public report.  Reading the result:  - `report.visibility: \"limited\"` means some pixels load through a tag manager or a store platform, so only part of the setup is visible from outside. It does not mean the tracking failed or is missing. - `status: \"warn\"` (browser-only) is the leak: the platform is tracked in the browser but not server-side. - `status: \"good\"` (server-side) means conversions reach the platform server-side, which recovers most of that signal. - `fixPrompt` is the same fix prompt the Conversion Leak Report page shows: this scan's findings, then the steps to send conversions server-side with `POST /v1/events` and to verify them. - `publicReport` links the host's public page on is-bleeding.com. A homepage scan that could read the site's pixels becomes that page's snapshot, the same as a scan on is-bleeding.com. Any other scan links the stored snapshot, taken at `scannedAt`, or returns null when the host has none.  Without a key, each IP address also shares one hourly ceiling with every other keyless caller. With a key, a user gets 60 scans a minute. 

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

