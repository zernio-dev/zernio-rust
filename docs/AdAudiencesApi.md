# \AdAudiencesApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_users_to_ad_audience**](AdAudiencesApi.md#add_users_to_ad_audience) | **POST** /v1/ads/audiences/{audienceId}/users | Add users to audience
[**create_ad_audience**](AdAudiencesApi.md#create_ad_audience) | **POST** /v1/ads/audiences | Create custom audience
[**delete_ad_audience**](AdAudiencesApi.md#delete_ad_audience) | **DELETE** /v1/ads/audiences/{audienceId} | Delete custom audience
[**get_ad_audience**](AdAudiencesApi.md#get_ad_audience) | **GET** /v1/ads/audiences/{audienceId} | Get audience details
[**list_ad_audiences**](AdAudiencesApi.md#list_ad_audiences) | **GET** /v1/ads/audiences | List custom audiences
[**replace_ad_audience_companies**](AdAudiencesApi.md#replace_ad_audience_companies) | **POST** /v1/ads/audiences/{audienceId}/companies | Replace audience companies
[**update_ad_audience**](AdAudiencesApi.md#update_ad_audience) | **PUT** /v1/ads/audiences/{audienceId} | Update an audience



## add_users_to_ad_audience

> models::AddUsersToAdAudience200Response add_users_to_ad_audience(audience_id, add_users_to_ad_audience_request)
Add users to audience

Upload user data to a customer_list audience. Data is SHA256-hashed server-side before sending to the platform. Email is used on every platform; phone is used on Meta only (other platforms ignore it). On TikTok and Pinterest, the first upload also provisions the audience (deferred create). LinkedIn uploads are full-replace. Max 10,000 users per request.  customer_list only. A LinkedIn `company_list` audience takes company rows, not people: send those to `POST /v1/ads/audiences/{audienceId}/companies`. This endpoint 422s for every other audience type. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**audience_id** | **String** | The Zernio audience id (the id field of GET /v1/ads/audiences), not the platform segment id. | [required] |
**add_users_to_ad_audience_request** | [**AddUsersToAdAudienceRequest**](AddUsersToAdAudienceRequest.md) |  | [required] |

### Return type

[**models::AddUsersToAdAudience200Response**](addUsersToAdAudience_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_ad_audience

> models::CreateAdAudience201Response create_ad_audience(create_ad_audience_request)
Create custom audience

Create a custom audience. `customer_list` is supported on Meta, Google, X, LinkedIn, TikTok, and Pinterest. `website` (pixel/tag visitors) and `lookalike` are supported on Meta, TikTok, Pinterest and Google. `meta_engagement` is Meta-only, `tiktok_engagement` TikTok-only, `pinterest_engagement` Pinterest-only; `company_list`, `engagement` and `website_retargeting` are LinkedIn-only. A type sent to a platform that does not support it is a 422 `FEATURE_NOT_AVAILABLE`.  Per-platform rules for `website`:  - Meta: `pixelId` required, `retentionDays` 1-180, optional `urlContains` or raw `rule`. `event` is not accepted. - TikTok: `pixelId` required, `retentionDays` one of 7, 14, 30, 60, 90, 180. `event` is a TikTok pixel event   (default `PAGE BROWSE`; also `CLICK BUTTON`, `PIXEL SUBMIT FORM`, `CONTACT`, `DOWNLOAD`,   `PIXEL ADD PAYMENT INFO`, `COMPLETE PAYMENT`, `INITIATE CHECKOUT`, `COMPLETE REGISTRATION`,   `PRODUCT DETAIL PAGE BROWSE`, `PIXEL SEARCH`, `PIXEL ADD TO CART`, `PLACE AN ORDER`,   `PIXEL ADD TO WISHLIST`, `PIXEL SUBSCRIBE`), optional `urlContains`. - Pinterest: `pixelId` is the Pinterest tag id, `retentionDays` 1-540, optional `event` (e.g. `checkout`, `addtocart`).   Pinterest matches URLs exactly, so `urlContains` is a 400 there. - Google: no `pixelId` (the account's Google tag is used), `retentionDays` 1-540, `urlContains`   defaults to `/` (all visitors). Built as a rule-based user list with prepopulation requested.  Per-platform rules for `lookalike`: Meta takes `ratio` (0.01-0.20); Pinterest takes `ratio` in whole percents (0.01-0.10) and `country` US, CA or GB; TikTok and Google take `size` (narrow, balanced, broad) instead of `ratio`. TikTok needs a seed with at least 1,000 matched people. `saved_targeting` stores a reusable TargetingSpec (no member upload, no adAccountId) that you reference later via `savedTargetingId` on `POST /v1/ads/create`.  How the audience gets filled depends on the type:  - `customer_list` is created empty. Add members with `POST /v1/ads/audiences/{audienceId}/users`.   On TikTok and Pinterest the audience is provisioned lazily on that first upload (until then its status is `pending`). - `company_list` is filled AT CREATION from the `companies` array below, which is required. To change the list   afterwards send the new full list to `POST /v1/ads/audiences/{audienceId}/companies` (a replace, not a merge).   The `/users` endpoint rejects these audiences with a 422. - `website`, `website_retargeting`, `engagement`, `meta_engagement`, `tiktok_engagement`, `pinterest_engagement`   and `lookalike` fill themselves from the pixel,   engagement source or seed audience you point them at. They take no member upload at all.  Create is not idempotent, never auto-retry. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_ad_audience_request** | [**CreateAdAudienceRequest**](CreateAdAudienceRequest.md) |  | [required] |

### Return type

[**models::CreateAdAudience201Response**](createAdAudience_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_ad_audience

> models::DeleteAccountGroup200Response delete_ad_audience(audience_id)
Delete custom audience

Removes the audience on its ad platform, then deletes the Zernio record. Meta, Google, TikTok, LinkedIn list and engagement segments, and X are deleted; Pinterest audiences and LinkedIn `website_retargeting` segments are archived, which is how those platforms remove them. `saved_targeting` audiences exist only on Zernio, so only the local record is removed.  If the platform refuses, the error is returned and the Zernio record is kept, so a retry is safe. An audience the platform no longer has counts as removed. Google Ads does not allow removing lookalike lists through its API, so those return 422 `FEATURE_NOT_AVAILABLE`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**audience_id** | **String** |  | [required] |

### Return type

[**models::DeleteAccountGroup200Response**](deleteAccountGroup_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad_audience

> models::GetAdAudience200Response get_ad_audience(audience_id)
Get audience details

Returns the local audience record and fresh data from Meta (if available).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**audience_id** | **String** | The Zernio audience id (the id field of GET /v1/ads/audiences), not the platform segment id. | [required] |

### Return type

[**models::GetAdAudience200Response**](getAdAudience_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ad_audiences

> models::ListAdAudiences200Response list_ad_audiences(account_id, ad_account_id, platform, r#type)
List custom audiences

Returns custom audiences for the given ad account. Supports Meta, Google, TikTok, Pinterest, LinkedIn, and X.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Account ID | [required] |
**ad_account_id** | **String** | Platform ad account ID | [required] |
**platform** | Option<**String**> |  |  |
**r#type** | Option<**String**> | Filter to one audience type. `saved_targeting` returns stored TargetingSpec audiences; the other types return uploaded/derived audiences. |  |

### Return type

[**models::ListAdAudiences200Response**](listAdAudiences_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## replace_ad_audience_companies

> models::ReplaceAdAudienceCompanies200Response replace_ad_audience_companies(audience_id, replace_ad_audience_companies_request)
Replace audience companies

Upload the company rows of a LinkedIn `company_list` audience (account-based marketing). LinkedIn-only, every other platform returns 422.  A LinkedIn audience segment holds exactly one uploaded list, so the list you send here REPLACES the segment's list instead of being appended to it: always send the full set of companies. LinkedIn returns only the identifier of the uploaded file, never its rows, so the merge cannot be done for you, keep the source list on your side.  How the matching behaves:  - Rows are plain text (not hashed), matched against LinkedIn's own company graph. - Matching is asynchronous: LinkedIn takes up to 48h for a new audience and up to 24h for a   later update, and the audience stays `processing` meanwhile. - LinkedIn does not document how quickly companies dropped from the list stop being targeted,   so treat removals as eventual rather than immediate. - LinkedIn recommends at least 1,000 companies for a usable match rate, and caps a list at   300,000.  The initial list is sent with `companies` on `POST /v1/ads/audiences`; this endpoint is for every change after that. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**audience_id** | **String** | The Zernio audience id (the id field of GET /v1/ads/audiences), not the platform segment id. | [required] |
**replace_ad_audience_companies_request** | [**ReplaceAdAudienceCompaniesRequest**](ReplaceAdAudienceCompaniesRequest.md) |  | [required] |

### Return type

[**models::ReplaceAdAudienceCompanies200Response**](replaceAdAudienceCompanies_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_ad_audience

> models::CreateAdAudience201Response update_ad_audience(audience_id, update_ad_audience_request)
Update an audience

Update an audience. `saved_targeting` audiences accept `name`, `description`, and `spec` (full replacement, no merge, Zernio-only, no platform call). Platform audiences (uploaded/website/lookalike) accept `name` and `description` only, updated on the platform first and then mirrored locally; their rules are immutable, so `spec` returns 400 for them. Platform audience updates are Meta-only for now (other platforms return 501). Ads already created from a saved_targeting audience are unaffected, they snapshot the targeting at creation. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**audience_id** | **String** |  | [required] |
**update_ad_audience_request** | [**UpdateAdAudienceRequest**](UpdateAdAudienceRequest.md) |  | [required] |

### Return type

[**models::CreateAdAudience201Response**](createAdAudience_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

