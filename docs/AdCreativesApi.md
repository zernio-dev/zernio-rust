# \AdCreativesApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_ad_creative**](AdCreativesApi.md#create_ad_creative) | **POST** /v1/ads/creatives | Create a standalone creative
[**delete_ad_creative**](AdCreativesApi.md#delete_ad_creative) | **DELETE** /v1/ads/creatives/{creativeId} | Delete a creative
[**delete_ad_video**](AdCreativesApi.md#delete_ad_video) | **DELETE** /v1/ads/videos/{videoId} | Delete an ad video
[**generate_ad_previews**](AdCreativesApi.md#generate_ad_previews) | **POST** /v1/ads/preview | Render pre-create ad previews
[**get_ad_creative**](AdCreativesApi.md#get_ad_creative) | **GET** /v1/ads/creatives/{creativeId} | Creative details
[**get_ad_media**](AdCreativesApi.md#get_ad_media) | **GET** /v1/ads/{adId}/media | Direct video and image URLs for an ad
[**get_ad_previews**](AdCreativesApi.md#get_ad_previews) | **GET** /v1/ads/{adId}/preview | Render previews of an existing ad
[**list_ad_catalog_product_sets**](AdCreativesApi.md#list_ad_catalog_product_sets) | **GET** /v1/ads/catalogs/{catalogId}/product-sets | List a catalog's product sets
[**list_ad_catalogs**](AdCreativesApi.md#list_ad_catalogs) | **GET** /v1/ads/catalogs | List Meta product catalogs
[**list_ad_creatives**](AdCreativesApi.md#list_ad_creatives) | **GET** /v1/ads/creatives | Creative library
[**list_ad_images**](AdCreativesApi.md#list_ad_images) | **GET** /v1/ads/images | Ad image library
[**list_ad_videos**](AdCreativesApi.md#list_ad_videos) | **GET** /v1/ads/videos | Ad video library
[**update_ad_creative**](AdCreativesApi.md#update_ad_creative) | **PUT** /v1/ads/creatives/{creativeId} | Rename a creative
[**upload_ad_image**](AdCreativesApi.md#upload_ad_image) | **POST** /v1/ads/images | Upload an ad image from base64
[**upload_ad_video**](AdCreativesApi.md#upload_ad_video) | **POST** /v1/ads/videos | Upload an ad video



## create_ad_creative

> models::CreateAdCreative201Response create_ad_creative(create_ad_creative_request)
Create a standalone creative

Creates a creative in the library WITHOUT an ad, reusable on the create endpoints via `existingCreativeId`. Provide exactly one of `imageUrl` (uploaded server-side), `imageHash` (from POST /v1/ads/images or the library list), or `carouselCards` (2-10 hand-built cards). The Page (and linked Instagram account, when present) is resolved from `accountId` as the story actor.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_ad_creative_request** | [**CreateAdCreativeRequest**](CreateAdCreativeRequest.md) |  | [required] |

### Return type

[**models::CreateAdCreative201Response**](createAdCreative_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_ad_creative

> models::DeleteAdCreative200Response delete_ad_creative(creative_id, account_id)
Delete a creative

Deletes a creative from the library. Meta only allows deleting creatives not referenced by any ad — otherwise its 400 surfaces verbatim.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**creative_id** | **String** | Platform creative id | [required] |
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. | [required] |

### Return type

[**models::DeleteAdCreative200Response**](deleteAdCreative_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_ad_video

> models::DeleteAdVideo200Response delete_ad_video(video_id, account_id, ad_account_id)
Delete an ad video

Removes a video from the ad account's video library. Meta's canonical `DELETE /{video_id}` fails with code 10 / subcode 1363055 for videos uploaded via `/act_X/advideos` even with `ads_management`; this endpoint uses the working account-scoped shape `DELETE /act_X/advideos?video_id=<id>` and returns Meta's `{success: true}` verbatim. Deleting a video that lives in a different ad account, or that Meta has already removed, returns Meta's error verbatim as a 4xx.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**video_id** | **String** | Meta ad video id (numeric). | [required] |
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. | [required] |
**ad_account_id** | **String** | Meta ad account id (act_<n>) that owns the video. | [required] |

### Return type

[**models::DeleteAdVideo200Response**](deleteAdVideo_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## generate_ad_previews

> models::GenerateAdPreviews200Response generate_ad_previews(generate_ad_previews_request)
Render pre-create ad previews

Renders how a creative would look per placement BEFORE any ad exists, via Meta's `/generatepreviews`. Provide exactly one creative source: `existingCreativeId` or `creativeSpec`. Each preview is an HTML `<iframe>` snippet embeddable directly. Unknown `formats` values return Meta's 400 verbatim. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**generate_ad_previews_request** | [**GenerateAdPreviewsRequest**](GenerateAdPreviewsRequest.md) |  | [required] |

### Return type

[**models::GenerateAdPreviews200Response**](generateAdPreviews_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad_creative

> models::GetAdCreative200Response get_ad_creative(creative_id, account_id, fields)
Creative details

One creative's details, verbatim from Meta. `fields` is a raw-passthrough override of the default projection.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**creative_id** | **String** | Platform creative id | [required] |
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. | [required] |
**fields** | Option<**String**> | Comma-separated Graph field override (supports nested {} projections). |  |

### Return type

[**models::GetAdCreative200Response**](getAdCreative_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad_media

> models::GetAdMedia200Response get_ad_media(ad_id)
Direct video and image URLs for an ad

Returns the direct signed URLs for every video and image asset used by an ad's live creative, normalised across shapes: single image/video, carousel, Reels/Story (`object_story_spec.video_data`) and dynamic creative (`asset_feed_spec`). Video items include Meta's poster thumbnail and the video's Meta id when available.  Reads Meta live rather than the stored creative blob because Meta's signed fbcdn URLs carry an `oe=<hex>` expiration (image_url ~24 h, video source ~12 d). Treat URLs as short-lived — re-fetch this endpoint before serving or downloading assets instead of caching URLs beyond that window.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_id** | **String** | Zernio ad id (24-char hex) or platform ad id. | [required] |

### Return type

[**models::GetAdMedia200Response**](getAdMedia_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad_previews

> models::GetAdPreviews200Response get_ad_previews(ad_id, formats)
Render previews of an existing ad

Renders an EXISTING ad per placement via Meta's `/{ad_id}/previews`. Each preview is an HTML `<iframe>` snippet embeddable directly. Unknown `formats` values return Meta's 400 verbatim. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_id** | **String** | Zernio ad id (24-char hex). | [required] |
**formats** | Option<**String**> | Comma-separated Meta ad_format values (max 10), one preview per format. Defaults to DESKTOP_FEED_STANDARD. |  |

### Return type

[**models::GetAdPreviews200Response**](getAdPreviews_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ad_catalog_product_sets

> models::ListAdCatalogProductSets200Response list_ad_catalog_product_sets(catalog_id, account_id)
List a catalog's product sets

Lists a Meta product catalog's product sets — the unit a catalog ad promotes. Pass the chosen set as `promotedObject.productSetId` on POST /v1/ads/create with `goal: catalog_sales`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**catalog_id** | **String** | Meta product catalog ID (from GET /v1/ads/catalogs) | [required] |
**account_id** | **String** | A facebook, instagram, or metaads social account ID | [required] |

### Return type

[**models::ListAdCatalogProductSets200Response**](listAdCatalogProductSets_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ad_catalogs

> models::ListAdCatalogs200Response list_ad_catalogs(account_id, ad_account_id)
List Meta product catalogs

Lists the Meta product catalogs reachable from an ad account (owned + agency-shared catalogs of the ad account's business), for Advantage+ catalog ads (`goal: catalog_sales` on POST /v1/ads/create — e.g. vehicle inventory catalogs). Read-only; uses scopes customers already granted (no reconnect needed). Catalog contents (items, feeds) are managed in Meta Commerce Manager, not through this API.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | A facebook, instagram, or metaads social account ID | [required] |
**ad_account_id** | **String** | Meta ad account ID (act_...) | [required] |

### Return type

[**models::ListAdCatalogs200Response**](listAdCatalogs_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ad_creatives

> models::ListAdCreatives200Response list_ad_creatives(account_id, ad_account_id, fields, limit, after)
Creative library

Lists the ad account's creative library (Meta's `/act_X/adcreatives`), rows returned verbatim. The default projection covers id, name, status, object type, thumbnail, object_story_spec / asset_feed_spec and url_tags; `fields` is a raw-passthrough override. Any creative id here is reusable on the create endpoints via `existingCreativeId`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. | [required] |
**ad_account_id** | **String** | Meta ad account id (act_<n>). | [required] |
**fields** | Option<**String**> | Comma-separated Graph field override (supports nested {} projections). |  |
**limit** | Option<**i32**> | Rows per page |  |[default to 25]
**after** | Option<**String**> | Cursor from paging.after of the previous page. |  |

### Return type

[**models::ListAdCreatives200Response**](listAdCreatives_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ad_images

> models::ListAdImages200Response list_ad_images(account_id, ad_account_id, fields, limit, after)
Ad image library

Lists the ad account's image library (Meta's `/act_X/adimages`), rows returned verbatim. The default projection covers hash, url, name, dimensions and status; `fields` is a raw-passthrough override. Any `hash` here is reusable wherever Meta accepts `image_hash` (e.g. `imageHash` on POST /v1/ads/creatives).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. | [required] |
**ad_account_id** | **String** | Meta ad account id (act_<n>). | [required] |
**fields** | Option<**String**> | Comma-separated Graph field override (supports nested {} projections). |  |
**limit** | Option<**i32**> | Rows per page |  |[default to 25]
**after** | Option<**String**> | Cursor from paging.after of the previous page. |  |

### Return type

[**models::ListAdImages200Response**](listAdImages_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ad_videos

> models::ListAdVideos200Response list_ad_videos(account_id, ad_account_id, fields, limit, after)
Ad video library

Lists the ad account's video library (Meta's `/act_X/advideos`), rows returned verbatim. The default projection covers id, title, status, poster frames and length; `fields` is a raw-passthrough override. Any `id` here is reusable as `video.id` on the create endpoints, so N ads that differ only in copy share one upload.  This is the only way to reach a video uploaded OUTSIDE Zernio (Ads Manager, another tool); videos we uploaded also come back as `creative.videoId` on GET /v1/ads.  Meta transcodes asynchronously, so a row is only usable once `status.video_status` reads `ready`. Upload a new video via POST /v1/ads/videos, or inline via `video.url` on POST /v1/ads/create.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. | [required] |
**ad_account_id** | **String** | Meta ad account id (act_<n>). | [required] |
**fields** | Option<**String**> | Comma-separated Graph field override (supports nested {} projections). |  |
**limit** | Option<**i32**> | Rows per page |  |[default to 25]
**after** | Option<**String**> | Cursor from paging.after of the previous page. |  |

### Return type

[**models::ListAdVideos200Response**](listAdVideos_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_ad_creative

> models::UpdateAdCreative200Response update_ad_creative(creative_id, update_ad_creative_request)
Rename a creative

Renames a creative. Creatives are immutable on Meta beyond `name` — for content changes create a new creative (POST /v1/ads/creatives) and swap it onto the ad (PUT /v1/ads/{adId} with `creative`).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**creative_id** | **String** | Platform creative id | [required] |
**update_ad_creative_request** | [**UpdateAdCreativeRequest**](UpdateAdCreativeRequest.md) |  | [required] |

### Return type

[**models::UpdateAdCreative200Response**](updateAdCreative_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## upload_ad_image

> models::UploadAdImage201Response upload_ad_image(upload_ad_image_request)
Upload an ad image from base64

Uploads raw image bytes to the Meta ad account's image library — for callers whose creatives aren't hosted at a public URL. Returns the image `hash` (Meta's identifier for the asset) and the Meta-hosted `url`, which can be used directly as `imageUrl` on the create endpoints. Max 30 MB decoded.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**upload_ad_image_request** | [**UploadAdImageRequest**](UploadAdImageRequest.md) |  | [required] |

### Return type

[**models::UploadAdImage201Response**](uploadAdImage_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## upload_ad_video

> models::UploadAdVideo201Response upload_ad_video(upload_ad_video_request)
Upload an ad video

Standalone ad-video upload (parallel to POST /v1/ads/images), so a video creative can be rendered via POST /v1/ads/preview or attached via `video.id` on POST /v1/ads/create before an ad exists.  Accepts either an https `videoUrl` we download server-side (SSRF-guarded) or raw `videoBase64` bytes; exactly one is required. `videoBase64` is capped by Vercel's body limit — around 4.5 MB payload in practice, so larger videos must come via `videoUrl`.  Returns the Meta `video.id` (reusable wherever `video.id` is accepted) plus Meta's auto-generated poster URL when available. The endpoint waits until Meta reports the video ready (chunked upload + transcode can take minutes; the handler runs up to 800 s).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**upload_ad_video_request** | [**UploadAdVideoRequest**](UploadAdVideoRequest.md) |  | [required] |

### Return type

[**models::UploadAdVideo201Response**](uploadAdVideo_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

