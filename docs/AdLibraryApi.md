# \AdLibraryApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**search_ad_library**](AdLibraryApi.md#search_ad_library) | **GET** /v1/ads/library | Search the public Ad Library



## search_ad_library

> models::SearchAdLibrary200Response search_ad_library(platform, account_id, q, page_ids, advertiser, countries, ad_type, status, platforms, media_type, languages, since, until, search_type, fields, limit, after)
Search the public Ad Library

Competitor and market research over the public ad archives. Meta's Ad Library (`GET /ads_archive`) is searched with Zernio's own developer access, so `platform=meta` needs no connected account at all. LinkedIn's Ad Library (`GET /rest/adLibrary`) runs on a connected `linkedin` / `linkedinads` account, passed as `accountId`. Passing a Meta account as `accountId` also selects Meta. Rows are returned in the platform's raw shape under `data`; `paging.after` is an opaque cursor on both (`null` when exhausted).  **Meta coverage.** Political and social-issue ads are searchable worldwide. Every other ad is in the archive only if it was delivered to the EU or UK within the last year, so a US-only commercial advertiser is invisible. Spend, impressions and demographics are political-only fields and are left out of the default projection; request them via `fields`. All customers share Zernio's Meta quota, so a `429` means back off for a minute.  **LinkedIn coverage.** Ads served after June 1 2023, worldwide, kept for a year after their last impression. EU-delivered ads carry impression ranges and the disclosed targeting facets. Pages are capped at 25 ads (`limit` > 25 is a 400); `after` is the next offset.  Which params apply: `q`, `countries`, `since`, `until`, `limit`, `after` on both; `pageIds`, `adType`, `status`, `platforms`, `mediaType`, `languages`, `searchType`, `fields` are Meta-only; `advertiser` is LinkedIn-only. Passing a param the account's platform does not support is a 400 naming the param.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**platform** | Option<**String**> | Which archive to search. `meta` needs no accountId. Required unless accountId is given. |  |
**account_id** | Option<**String**> | Zernio SocialAccount id. Required for LinkedIn (linkedin / linkedinads: its token searches). Optional for Meta, where any facebook / instagram / metaads account only selects the platform. |  |
**q** | Option<**String**> | Keyword search. Meta does not translate it, so write it in the ads' language. Required unless pageIds (Meta) or advertiser (LinkedIn) is given. |  |
**page_ids** | Option<**String**> | Meta only. Comma-separated Facebook Page ids (max 10) whose ads to list. |  |
**advertiser** | Option<**String**> | LinkedIn only. Advertiser (Page) name to search. |  |
**countries** | Option<**String**> | Comma-separated ISO 3166-1 alpha-2 codes the ads reached. Meta defaults to ALL (an explicit ALL is Meta-only); LinkedIn searches every market when omitted. |  |
**ad_type** | Option<**String**> | Meta only. |  |[default to ALL]
**status** | Option<**String**> | Meta only. ACTIVE = eligible for delivery right now. |  |[default to ACTIVE]
**platforms** | Option<**String**> | Meta only. Comma-separated publisher platforms: FACEBOOK, INSTAGRAM, AUDIENCE_NETWORK, MESSENGER, WHATSAPP, OCULUS, THREADS, STREAMING_SERVICES. |  |
**media_type** | Option<**String**> | Meta only. |  |
**languages** | Option<**String**> | Meta only. Comma-separated ISO 639-1 codes of the ad text. |  |
**since** | Option<**String**> | Earliest delivery date (YYYY-MM-DD). |  |
**until** | Option<**String**> | Latest delivery date (YYYY-MM-DD). |  |
**search_type** | Option<**String**> | Meta only. Whether q matches words in any order or as an exact phrase (comma-separate phrases to match all of them). |  |[default to KEYWORD_UNORDERED]
**fields** | Option<**String**> | Meta only. Comma-separated Graph field override. Supports nested {} projections and Graph field modifiers, so a nested edge can be paged explicitly: without a .limit() modifier the expansion runs at the Meta default page size and the tail is dropped silently. |  |
**limit** | Option<**i32**> | Rows per page. LinkedIn accepts at most 25. |  |[default to 25]
**after** | Option<**String**> | paging.after of the previous page. |  |

### Return type

[**models::SearchAdLibrary200Response**](searchAdLibrary_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

