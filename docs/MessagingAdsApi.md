# \MessagingAdsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_call_ad**](MessagingAdsApi.md#create_call_ad) | **POST** /v1/ads/call | Create Click-to-Call ad
[**create_ctwa_ad**](MessagingAdsApi.md#create_ctwa_ad) | **POST** /v1/ads/ctwa | Create Click-to-WhatsApp ad (deprecated)
[**create_messaging_ad**](MessagingAdsApi.md#create_messaging_ad) | **POST** /v1/ads/messaging | Create click-to-message ad (WhatsApp / Messenger / Instagram Direct)



## create_call_ad

> create_call_ad(create_call_ad_request)
Create Click-to-Call ad

Same shape and flow as POST /v1/ads/ctwa, but the CTA is CALL_NOW dialing `phoneNumber` via a tel: link. The ad set is destination_type PHONE_CALL optimizing QUALITY_CALL and the campaign objective defaults to OUTCOME_LEADS. Supports the same single-creative and multi-creative shapes as CTWA.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_call_ad_request** | [**CreateCallAdRequest**](CreateCallAdRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_ctwa_ad

> models::CreateCtwaAd201Response create_ctwa_ad(ctwa_ad_request_body)
Create Click-to-WhatsApp ad (deprecated)

Deprecated: use POST /v1/ads/messaging with `destination: whatsapp`. This endpoint stays available for back-compat; no removal planned.  Creates one or more Click-to-WhatsApp (CTWA) ads on Meta under a single campaign and ad set. When tapped, each ad opens a WhatsApp conversation with the business attached to the supplied Facebook Page. The full hierarchy (campaign, ad set, creative(s), ad(s)) is created and activated in one call. The CTA is locked to WHATSAPP_MESSAGE and the destination is hard-coded to api.whatsapp.com/send; Meta resolves the actual WhatsApp number from the Page-to-WA pairing configured in Page settings or Business Manager.  Supports two mutually-exclusive shapes:  - **Single-creative**: supply top-level `headline`, `body`, and one of `imageUrl` / `video`. Creates 1 campaign + 1 ad set + 1 ad.  - **Multi-creative**: supply a `creatives[]` array with N entries (each carrying its own headline, body, and image/video). Creates 1 campaign + 1 ad set + N ads sharing budget and targeting so Meta A/Bs the creatives inside a single auction instead of fragmenting budget across N parallel campaigns. Recommended when launching multiple creative variants for the same campaign.  Prerequisites enforced by Meta (surfaced as platform_error on failure): the Facebook Page must be paired with a verified WhatsApp Business number, the WhatsApp Business Account must be business-verified, and the Meta access token must carry ads_management.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ctwa_ad_request_body** | [**CtwaAdRequestBody**](CtwaAdRequestBody.md) |  | [required] |

### Return type

[**models::CreateCtwaAd201Response**](createCtwaAd_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_messaging_ad

> create_messaging_ad(create_messaging_ad_request)
Create click-to-message ad (WhatsApp / Messenger / Instagram Direct)

Creates a click-to-message ad; `destination` selects where the tapped ad opens a conversation: WhatsApp, the Page's Messenger inbox or the linked Instagram account's Direct inbox. The ad set is created with the matching destination_type and CONVERSATIONS optimization; the campaign objective defaults to OUTCOME_ENGAGEMENT. Supports single-creative and multi-creative shapes. Supersedes POST /v1/ads/ctwa (deprecated, equivalent to `destination: whatsapp`).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_messaging_ad_request** | [**CreateMessagingAdRequest**](CreateMessagingAdRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

