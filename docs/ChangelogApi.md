# \ChangelogApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**list_changelog**](ChangelogApi.md#list_changelog) | **GET** /v1/changelog | List API changelog entries



## list_changelog

> models::ListChangelog200Response list_changelog(r#type, impact, platform, before, limit)
List API changelog entries

The API changelog, newest first. No API key needed; one address may make 120 requests a minute. Each entry is what the `api.changelog.published` webhook delivered: the announcement in `message`, its `impact` on existing integrations, and in `changes` the deterministic diff of the OpenAPI spec (operations and schemas added, removed and modified) for automation to act on. Page with `before` set to the previous page's `nextCursor`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**r#type** | Option<**String**> | Only entries of this type. |  |
**impact** | Option<**String**> | Only entries with this impact. `action_required` lists the changes an integration may need to act on. |  |
**platform** | Option<**String**> | Only entries tagged with this platform or area slug (see `platforms` on the entry). One slug per request. |  |
**before** | Option<**String**> | Only entries published strictly before this instant. Pass the previous page's `nextCursor`. |  |
**limit** | Option<**i32**> |  |  |[default to 20]

### Return type

[**models::ListChangelog200Response**](listChangelog_200_response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

