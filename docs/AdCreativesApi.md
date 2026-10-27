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
[**get_ad_video_status**](AdCreativesApi.md#get_ad_video_status) | **GET** /v1/ads/videos/{videoId} | Get ad video processing status
[**list_ad_creatives**](AdCreativesApi.md#list_ad_creatives) | **GET** /v1/ads/creatives | Creative library
[**list_ad_images**](AdCreativesApi.md#list_ad_images) | **GET** /v1/ads/images | Ad image library
[**list_ad_videos**](AdCreativesApi.md#list_ad_videos) | **GET** /v1/ads/videos | Ad video library
[**list_ads_tik_tok_identities**](AdCreativesApi.md#list_ads_tik_tok_identities) | **GET** /v1/ads/tiktok-identities | List TikTok ad identities
[**list_partnership_ad_content**](AdCreativesApi.md#list_partnership_ad_content) | **GET** /v1/ads/partnership-content | List partnership ad content
[**list_partnership_ad_permissions**](AdCreativesApi.md#list_partnership_ad_permissions) | **GET** /v1/ads/partnership-permissions | List partnership permissions
[**set_partnership_ad_permission**](AdCreativesApi.md#set_partnership_ad_permission) | **POST** /v1/ads/partnership-permissions | Set partnership permission
[**update_ad_creative**](AdCreativesApi.md#update_ad_creative) | **PUT** /v1/ads/creatives/{creativeId} | Rename a creative
[**upload_ad_image**](AdCreativesApi.md#upload_ad_image) | **POST** /v1/ads/images | Upload an ad image from base64
[**upload_ad_video**](AdCreativesApi.md#upload_ad_video) | **POST** /v1/ads/videos | Upload an ad video



## create_ad_creative

> models::CreateAdCreative201Response create_ad_creative(create_ad_creative_request)
Create a standalone creative

Creates a reusable Meta creative from an image or carousel without creating an ad, ready to attach to ads later.  Creates a creative in the library WITHOUT an ad, reusable on the create endpoints via `existingCreativeId`. Provide exactly one of `imageUrl` (uploaded server-side), `imageHash` (from POST /v1/ads/images or the library list), or `carouselCards` (2-10 hand-built cards). The Page (and linked Instagram account, when present) is resolved from `accountId` as the story actor. `creativeFeatures` configures Advantage+ enhancements. `promotion` is not supported and any object is rejected with 400.

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

Deletes a Meta creative from the library, which Meta only allows when no ad uses it.  Meta only allows deleting creatives not referenced by any ad; otherwise its 400 surfaces verbatim. 

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

Removes a video from a Meta ad account's video library.  Meta's canonical `DELETE /{video_id}` fails with code 10 / subcode 1363055 for videos uploaded via `/act_X/advideos` even with `ads_management`; this endpoint uses the working account-scoped shape `DELETE /act_X/advideos?video_id=<id>` and returns Meta's `{success: true}` verbatim. Deleting a video that lives in a different ad account, or that Meta has already removed, returns Meta's error verbatim as a 4xx. 

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

Shows how a Meta creative will look in each placement before you create the ad, as embeddable previews.  Renders how a creative would look per placement BEFORE any ad exists, via Meta's `/generatepreviews`. Provide exactly one creative source: `existingCreativeId` or `creativeSpec`. Each preview is an HTML `<iframe>` snippet embeddable directly. Unknown `formats` values return Meta's 400 verbatim. 

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

> models::GetAdCreative200Response get_ad_creative(creative_id, account_id, fields, thumbnail_width, thumbnail_height)
Creative details

Shows the details of one Meta creative, such as its content, status and thumbnail.  One creative's details, verbatim from Meta. `fields` is a raw-passthrough override of the default projection.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**creative_id** | **String** | Platform creative id | [required] |
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. | [required] |
**fields** | Option<**String**> | Comma-separated Graph field override. Supports nested {} projections and Graph field modifiers, so a nested edge can be paged explicitly: without a .limit() modifier the expansion runs at the Meta default page size and the tail is dropped silently. |  |
**thumbnail_width** | Option<**i32**> | Width in pixels of the `thumbnail_url` rendering, forwarded to Meta as `thumbnail_width`. Without it Meta returns a 64x64 thumbnail. |  |
**thumbnail_height** | Option<**i32**> | Height in pixels of the `thumbnail_url` rendering, forwarded to Meta as `thumbnail_height`. Without it Meta returns a 64x64 thumbnail. |  |

### Return type

[**models::GetAdCreative200Response**](getAdCreative_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad_media

> models::GetAdMedia200Response get_ad_media(ad_id, account_id)
Direct video and image URLs for an ad

Returns fresh, short-lived download links for every image and video a Meta ad uses, including the original media of a boosted Instagram post.  Returns the direct signed URLs for every video and image asset used by an ad's live creative, normalised across shapes: single image/video, carousel, Reels/Story (`object_story_spec.video_data`) and dynamic creative (`asset_feed_spec`). Video items include Meta's poster thumbnail and the video's Meta id when available.  Boosted Instagram posts (creatives with no image of their own) return the original post's media: the image, the video with its cover as `thumbnailUrl`, or every child of a carousel post with `index`. When the connection cannot read the Instagram post, the item is a 1080px rendering of the creative instead.  Reads Meta live rather than the stored creative blob because Meta's signed fbcdn URLs carry an `oe=<hex>` expiration (image_url ~24 h, video source ~12 d). Treat URLs as short-lived: re-fetch this endpoint before serving or downloading assets instead of caching URLs beyond that window.  **Meta ads that are not synced yet.** Pass `accountId` with a Meta platform ad id that is not in Zernio's store to read its media live through that connection; the response carries `synced: false`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_id** | **String** | Zernio ad id (24-char hex) or platform ad id. | [required] |
**account_id** | Option<**String**> | Meta only. A Zernio connection id (Meta Ads or Facebook connection) used when `{adId}` is a Meta ad id that is not in Zernio's synced store, for example an ad created in Ads Manager on an ad account reached only through a Facebook connection. The ad is then read live from Meta through that connection and the response carries `synced: false`. The same rules as GET /v1/ads/campaigns/{campaignId} apply: a connection on a profile the API key cannot access answers 404, and an ad on an ad account outside the connection's selected ad accounts answers 403 `ad_account_not_selected`. An id Meta cannot read through the connection, or that is not an ad (a campaign or ad set id, for example), answers 404 `ad_not_found`, and a connection that is not Meta answers 501. Ads Meta reports as DELETED are returned too, with their status. Ignored when the ad is in the store (the stored ad's own connection is used). Without it an unsynced ad answers 404 `ad_not_found`. Writes (PUT, DELETE, status) still need the ad in the store. |  |

### Return type

[**models::GetAdMedia200Response**](getAdMedia_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad_previews

> models::GetAdPreviews200Response get_ad_previews(ad_id, account_id, formats)
Render previews of an existing ad

Shows how an existing Meta ad looks in each placement, as embeddable previews.  Renders an EXISTING ad per placement via Meta's `/{ad_id}/previews`. Each preview is an HTML `<iframe>` snippet embeddable directly. Unknown `formats` values return Meta's 400 verbatim.  **Meta ads that are not synced yet.** Pass `accountId` with a Meta platform ad id that is not in Zernio's store to render it live through that connection; the response carries `synced: false`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_id** | **String** | Zernio ad id (24-char hex) or Meta platform ad id. | [required] |
**account_id** | Option<**String**> | Meta only. A Zernio connection id (Meta Ads or Facebook connection) used when `{adId}` is a Meta ad id that is not in Zernio's synced store, for example an ad created in Ads Manager on an ad account reached only through a Facebook connection. The ad is then read live from Meta through that connection and the response carries `synced: false`. The same rules as GET /v1/ads/campaigns/{campaignId} apply: a connection on a profile the API key cannot access answers 404, and an ad on an ad account outside the connection's selected ad accounts answers 403 `ad_account_not_selected`. An id Meta cannot read through the connection, or that is not an ad (a campaign or ad set id, for example), answers 404 `ad_not_found`, and a connection that is not Meta answers 501. Ads Meta reports as DELETED are returned too, with their status. Ignored when the ad is in the store (the stored ad's own connection is used). Without it an unsynced ad answers 404 `ad_not_found`. Writes (PUT, DELETE, status) still need the ad in the store. |  |
**formats** | Option<**String**> | Comma-separated Meta ad_format values (max 10), one preview per format. Defaults to DESKTOP_FEED_STANDARD. |  |

### Return type

[**models::GetAdPreviews200Response**](getAdPreviews_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad_video_status

> models::GetAdVideoStatus200Response get_ad_video_status(video_id, account_id, ad_account_id)
Get ad video processing status

Checks whether an uploaded Meta ad video has finished processing and is ready to use in an ad.  Reads a video's processing state live from Meta (`GET /{video-id}?fields=status`). Poll this after `POST /v1/ads/videos` with `async: true` until `status` is `ready`; the video is only usable as `video.id` on the create endpoints from then on.  `status` is normalised: `ready`, `error` (Meta's `error` or `expired`), and `processing` for every other Meta state. `platformStatus` carries Meta's raw `video_status` and `processingProgress` Meta's 0-100 percentage when it reports one. Polling every 5 to 10 seconds is plenty.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**video_id** | **String** | Meta ad video id (numeric). | [required] |
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. | [required] |
**ad_account_id** | **String** | Meta ad account id (act_<n>) the video was uploaded to. | [required] |

### Return type

[**models::GetAdVideoStatus200Response**](getAdVideoStatus_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ad_creatives

> models::ListAdCreatives200Response list_ad_creatives(account_id, ad_account_id, fields, limit, after)
Creative library

Lists the creatives saved in a Meta ad account so you can reuse one in a new ad.  Lists the ad account's creative library (Meta's `/act_X/adcreatives`), rows returned verbatim. The default projection covers id, name, status, object type, thumbnail, object_story_spec / asset_feed_spec and url_tags; `fields` is a raw-passthrough override. Any creative id here is reusable on the create endpoints via `existingCreativeId`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. | [required] |
**ad_account_id** | **String** | Meta ad account id (act_<n>). | [required] |
**fields** | Option<**String**> | Comma-separated Graph field override. Supports nested {} projections and Graph field modifiers, so a nested edge can be paged explicitly: without a .limit() modifier the expansion runs at the Meta default page size and the tail is dropped silently. |  |
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

Lists the images in a Meta ad account's library so you can reuse one in a creative.  Lists the ad account's image library (Meta's `/act_X/adimages`), rows returned verbatim. The default projection covers hash, url, name, dimensions and status; `fields` is a raw-passthrough override. Any `hash` here is reusable wherever Meta accepts `image_hash` (e.g. `imageHash` on POST /v1/ads/creatives).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. | [required] |
**ad_account_id** | **String** | Meta ad account id (act_<n>). | [required] |
**fields** | Option<**String**> | Comma-separated Graph field override. Supports nested {} projections and Graph field modifiers, so a nested edge can be paged explicitly: without a .limit() modifier the expansion runs at the Meta default page size and the tail is dropped silently. |  |
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

Lists the videos in a Meta ad account's library, including ones uploaded elsewhere, so you can reuse one across ads.  Lists the ad account's video library (Meta's `/act_X/advideos`), rows returned verbatim. The default projection covers id, title, status, poster frames, length and `source` (the playable MP4); `fields` is a raw-passthrough override. Any `id` here is reusable as `video.id` on the create endpoints, so N ads that differ only in copy share one upload.  `source` lets you PLAY a video before picking it, which a poster frame alone can't settle when several videos share a first frame. It is a signed CDN URL that EXPIRES, so treat it as good for preview at selection time only. Never persist it; re-list to get a fresh one.  This is the only way to reach a video uploaded OUTSIDE Zernio (Ads Manager, another tool); videos we uploaded also come back as `creative.videoId` on GET /v1/ads.  Meta transcodes asynchronously, so a row is only usable once `status.video_status` reads `ready`. Upload a new video via POST /v1/ads/videos, or inline via `video.url` on POST /v1/ads/create.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. | [required] |
**ad_account_id** | **String** | Meta ad account id (act_<n>). | [required] |
**fields** | Option<**String**> | Comma-separated Graph field override. Supports nested {} projections and Graph field modifiers, so a nested edge can be paged explicitly: without a .limit() modifier the expansion runs at the Meta default page size and the tail is dropped silently. |  |
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


## list_ads_tik_tok_identities

> models::ListAdsTikTokIdentities200Response list_ads_tik_tok_identities(account_id, ad_account_id)
List TikTok ad identities

The identities an ad on this TikTok advertiser may run as (the profile shown on the ad): the advertiser's own TikTok accounts (TT_USER), Business Center authorized accounts (BC_AUTH_TT) and custom brand identities (CUSTOMIZED_USER). Pass the chosen `identityId` on POST /v1/ads/create or POST /v1/ads/boost. Spark-post identities (AUTH_CODE) are not listed; a Spark code creates its own.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | A tiktok or tiktokads account ID | [required] |
**ad_account_id** | **String** | TikTok advertiser ID | [required] |

### Return type

[**models::ListAdsTikTokIdentities200Response**](listAdsTikTokIdentities_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_partnership_ad_content

> models::ListPartnershipAdContent200Response list_partnership_ad_content(account_id, creator_username, post_url, only_allowlisted)
List partnership ad content

Lists a creator's Instagram posts you can run as Partnership Ads, looked up by creator or post link (private beta).  Lists creator Instagram posts available to the advertiser for Partnership Ads. Supply creatorUsername or postUrl. Requires instagram_branded_content_ads_brand permission and an advertiser Instagram Business Account. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount ID. | [required] |
**creator_username** | Option<**String**> | Creator username. Required unless postUrl is supplied. |  |
**post_url** | Option<**String**> | Instagram post permalink. Required unless creatorUsername is supplied. |  |
**only_allowlisted** | Option<**bool**> | Return only creators with account-level permission. |  |

### Return type

[**models::ListPartnershipAdContent200Response**](listPartnershipAdContent_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_partnership_ad_permissions

> models::ListPartnershipAdPermissions200Response list_partnership_ad_permissions(account_id, creator_username)
List partnership permissions

Lists the creators who have granted, or have pending, permission for your Instagram account to run Partnership Ads with them (private beta).  Lists granted or pending creator permissions for the advertiser Instagram Business Account. Requires instagram_branded_content_ads_brand permission. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount ID. | [required] |
**creator_username** | Option<**String**> | Filter by creator username. |  |

### Return type

[**models::ListPartnershipAdPermissions200Response**](listPartnershipAdPermissions_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## set_partnership_ad_permission

> models::SetPartnershipAdPermission200Response set_partnership_ad_permission(set_partnership_ad_permission_request)
Set partnership permission

Asks a creator for permission to run Partnership Ads with their content, or revokes it (private beta).  Requests permission from a creator or revokes it when revoke is true. Requests require the creator to approve in Instagram. Requires instagram_branded_content_ads_brand permission. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**set_partnership_ad_permission_request** | [**SetPartnershipAdPermissionRequest**](SetPartnershipAdPermissionRequest.md) |  | [required] |

### Return type

[**models::SetPartnershipAdPermission200Response**](setPartnershipAdPermission_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_ad_creative

> models::UpdateAdCreative200Response update_ad_creative(creative_id, update_ad_creative_request)
Rename a creative

Renames a Meta creative (Meta does not allow other changes, so make a new creative to change its content).  Creatives are immutable on Meta beyond `name`. For content changes create a new creative (POST /v1/ads/creatives) and swap it onto the ad (PUT /v1/ads/{adId} with `creative`). 

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

Uploads an image file to a Meta ad account's library, for creatives that are not hosted at a public URL.  Returns the image `hash` (Meta's identifier for the asset) and the Meta-hosted `url`, which can be used directly as `imageUrl` on the create endpoints. Max 30 MB decoded. 

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

Uploads a video to a Meta ad account from a URL or file, so you can preview it or use it in ads before any ad exists.  Standalone ad-video upload (parallel to POST /v1/ads/images), so a video creative can be rendered via POST /v1/ads/preview or attached via `video.id` on POST /v1/ads/create before an ad exists.  Accepts either an https `videoUrl` we download server-side (SSRF-guarded) or raw `videoBase64` bytes; exactly one is required. `videoBase64` is capped by Vercel's body limit, around 4.5 MB payload in practice, so larger videos must come via `videoUrl`.  Returns the Meta `video.id` (reusable wherever `video.id` is accepted) plus Meta's auto-generated poster URL when available. By default the endpoint waits until Meta reports the video ready (chunked upload + transcode can take minutes; the handler runs up to 800 s) and answers 201.  **Async mode.** Send `async: true` to get a 202 as soon as Meta has accepted the bytes, with `video.status: processing`. Then either poll `GET /v1/ads/videos/{videoId}` until `status` is `ready`, or subscribe to the `ad.video.processed` webhook. A create call that references the video while it is still processing waits up to 30 s, then answers 409 `invalid_resource_state` naming the status endpoint. With `videoUrl` the download and byte transfer still happen inside the request; only Meta's transcode is skipped.

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

