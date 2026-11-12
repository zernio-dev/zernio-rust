# \CreatorPortalApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_creator_payout_login**](CreatorPortalApi.md#create_creator_payout_login) | **POST** /public/creator-campaigns/{token}/payout-login | Open the creator's Stripe dashboard
[**get_creator_payout_statement**](CreatorPortalApi.md#get_creator_payout_statement) | **GET** /public/creator-campaigns/{token}/payouts/{transferId}/statement | Download a payout statement
[**get_creator_payouts**](CreatorPortalApi.md#get_creator_payouts) | **GET** /public/creator-campaigns/{token}/payouts | List a creator's earnings history
[**get_creator_portal**](CreatorPortalApi.md#get_creator_portal) | **GET** /public/creator-campaigns/{token} | Read a creator invite or participant page
[**join_creator_campaign**](CreatorPortalApi.md#join_creator_campaign) | **POST** /public/creator-campaigns/{token} | Join a campaign
[**presign_creator_draft_upload**](CreatorPortalApi.md#presign_creator_draft_upload) | **POST** /public/creator-campaigns/{token}/drafts/upload | Get an upload URL for a draft
[**recover_creator_portal_links**](CreatorPortalApi.md#recover_creator_portal_links) | **POST** /public/creator-campaigns/recover-link | Email a creator their campaign links
[**remove_creator_account**](CreatorPortalApi.md#remove_creator_account) | **DELETE** /public/creator-campaigns/{token}/accounts/{accountId} | Remove a connected account
[**request_creator_sample**](CreatorPortalApi.md#request_creator_sample) | **POST** /public/creator-campaigns/{token}/samples | Request a product sample
[**set_creator_spark_code**](CreatorPortalApi.md#set_creator_spark_code) | **PUT** /public/creator-campaigns/{token}/submissions/{submissionId}/spark-code | Set a post's Spark code
[**start_creator_connect**](CreatorPortalApi.md#start_creator_connect) | **POST** /public/creator-campaigns/{token}/connect | Start connecting a creator account
[**start_creator_payouts**](CreatorPortalApi.md#start_creator_payouts) | **POST** /public/creator-campaigns/{token}/payouts | Start payout onboarding
[**submit_creator_draft**](CreatorPortalApi.md#submit_creator_draft) | **POST** /public/creator-campaigns/{token}/drafts | Submit a draft for review
[**submit_creator_post**](CreatorPortalApi.md#submit_creator_post) | **POST** /public/creator-campaigns/{token}/submissions | Submit a post



## create_creator_payout_login

> models::CreateCreatorPayoutLogin200Response create_creator_payout_login(token)
Open the creator's Stripe dashboard

Returns a one-time link into the creator's Stripe Express dashboard, where they change bank details and see each payout. Only after the creator submitted their payout details. About 20 attempts per participant every 10 minutes. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**token** | **String** | A participant token or an open invite token. A malformed token answers 404 like an unknown one. | [required] |

### Return type

[**models::CreateCreatorPayoutLogin200Response**](createCreatorPayoutLogin_200_response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_creator_payout_statement

> std::path::PathBuf get_creator_payout_statement(token, transfer_id)
Download a payout statement

A PDF statement of one paid payout to this creator: who paid, the campaign, the date, the amount and the Stripe transfer id. It is a statement of a payment, not a tax invoice.  Only for a paid payout of this participant; anything else answers 404.  About 60 downloads per participant every 10 minutes. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**token** | **String** | A participant token or an open invite token. A malformed token answers 404 like an unknown one. | [required] |
**transfer_id** | **String** |  | [required] |

### Return type

[**std::path::PathBuf**](std::path::PathBuf.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/pdf, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_creator_payouts

> models::GetCreatorPayouts200Response get_creator_payouts(token, limit, skip)
List a creator's earnings history

The participant's ledger entries, newest first, with the bucket each one moved money from and to (`accruing`, `owed`, `payable`, `settling`, `settled`; null for the other side), plus the payout setup. Never cached. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**token** | **String** | A participant token or an open invite token. A malformed token answers 404 like an unknown one. | [required] |
**limit** | Option<**i32**> |  |  |[default to 50]
**skip** | Option<**i32**> |  |  |[default to 0]

### Return type

[**models::GetCreatorPayouts200Response**](getCreatorPayouts_200_response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_creator_portal

> models::GetCreatorPortal200Response get_creator_portal(token)
Read a creator invite or participant page

What a creator sees behind a campaign link, with no API key. Never cached.  `token` is one of:  - An open invite token (from `POST /v1/creator-campaigns/{campaignId}/invite-link`): answers `kind: invite` with the campaign only. - A participant token (from an invite or a join): answers `kind: participant` with the creator's connected accounts, latest 100 submissions, draft versions, sample requests, earnings and payout setup. A creator held for approval reads it with `participant.status` `pending` (or `denied` once turned away).  Reading a participant page also re-checks the creator's connected accounts. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**token** | **String** | A participant token or an open invite token. A malformed token answers 404 like an unknown one. | [required] |

### Return type

[**models::GetCreatorPortal200Response**](getCreatorPortal_200_response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## join_creator_campaign

> models::JoinCreatorCampaign201Response join_creator_campaign(token, join_creator_campaign_request)
Join a campaign

Accepts a participant invite, or joins through an open invite link.  - Participant token: the body is ignored and the invite is accepted. - Open invite token: a new participant is created from `displayName` (required) and `email` (optional), and a fresh participant token comes back. Keep it: it is the creator's only key to their page. - On a campaign with `joinApproval: manual`, an open-link joiner lands `pending` and `campaign_participant.pending` fires instead of `campaign_participant.joined`. A pending creator holds no place under `caps.maxParticipants` (the limit is checked when the operator approves them) and cannot submit posts, drafts or sample requests until approved. Personal invites always get straight in.  Open-link joins are limited to about 20 per IP address and 60 per link every 10 minutes. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**token** | **String** | A participant token or an open invite token. A malformed token answers 404 like an unknown one. | [required] |
**join_creator_campaign_request** | Option<[**JoinCreatorCampaignRequest**](JoinCreatorCampaignRequest.md)> |  |  |

### Return type

[**models::JoinCreatorCampaign201Response**](joinCreatorCampaign_201_response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## presign_creator_draft_upload

> models::PresignCreatorDraftUpload200Response presign_creator_draft_upload(token, presign_creator_draft_upload_request)
Get an upload URL for a draft

Returns a presigned URL to upload one draft file to, on a campaign with `requireDraftApproval`. `PUT` the file to `uploadUrl` with the same `Content-Type`, then pass `publicUrl` as `mediaUrl` to `POST /public/creator-campaigns/{token}/drafts`. The URL expires after `expiresIn` seconds.  Accepted files: MP4, MOV or WebM video, JPG, PNG or WebP image, up to 500 MB. About 20 uploads per participant every 10 minutes. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**token** | **String** | A participant token or an open invite token. A malformed token answers 404 like an unknown one. | [required] |
**presign_creator_draft_upload_request** | [**PresignCreatorDraftUploadRequest**](PresignCreatorDraftUploadRequest.md) |  | [required] |

### Return type

[**models::PresignCreatorDraftUpload200Response**](presignCreatorDraftUpload_200_response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## recover_creator_portal_links

> models::RecoverCreatorPortalLinks202Response recover_creator_portal_links(recover_creator_portal_links_request)
Email a creator their campaign links

For a creator who lost their link. Emails every personal participant link held by `email` in one message, optionally only the one for `campaignId`.  - Removed participants and draft campaigns are left out. - Always answers 202 with the same body, so the answer never tells whether the address has links. - Limited to 5 requests per hour per email address and 5 per hour per IP address. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**recover_creator_portal_links_request** | [**RecoverCreatorPortalLinksRequest**](RecoverCreatorPortalLinksRequest.md) |  | [required] |

### Return type

[**models::RecoverCreatorPortalLinks202Response**](recoverCreatorPortalLinks_202_response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_creator_account

> models::RemoveCreatorAccount200Response remove_creator_account(token, account_id)
Remove a connected account

Disconnects one of the creator's accounts. The account belongs to the creator, not to one campaign, so it stops counting in every campaign of this brand they joined.  What its posts already earned stays: accrued, approved and paid amounts are not touched.  Refused while a post from the account is still counting views, because those views are read through the account. It can be removed once their tracking ends. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**token** | **String** | A participant token or an open invite token. A malformed token answers 404 like an unknown one. | [required] |
**account_id** | **String** | The `id` of one of the participant's `accounts`. | [required] |

### Return type

[**models::RemoveCreatorAccount200Response**](removeCreatorAccount_200_response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## request_creator_sample

> models::RequestCreatorSample201Response request_creator_sample(token, request_creator_sample_request)
Request a product sample

Asks for a free sample of one of the campaign's `sampleProducts`, shipped to `shippingAddress`, and fires `campaign_sample.requested`. The request waits for the campaign team; on approval the creator gets a single-use discount code for the product.  - A product with `variants` needs `variantId`. - One open request per product: asking again while one is pending, approved or shipped answers 409. A declined product can be asked again.  About 10 requests per participant every 10 minutes. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**token** | **String** | A participant token or an open invite token. A malformed token answers 404 like an unknown one. | [required] |
**request_creator_sample_request** | [**RequestCreatorSampleRequest**](RequestCreatorSampleRequest.md) |  | [required] |

### Return type

[**models::RequestCreatorSample201Response**](requestCreatorSample_201_response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## set_creator_spark_code

> models::SetCreatorSparkCode200Response set_creator_spark_code(token, submission_id, set_creator_spark_code_request)
Set a post's Spark code

The creator pastes the Spark code of one of their TikTok posts (generated in the TikTok app under the post's ad settings), so the brand can run the post as a Spark Ad under the creator's handle.  Send `null` to clear it. The code is never returned: submissions only expose `hasSparkCode`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**token** | **String** | A participant token or an open invite token. A malformed token answers 404 like an unknown one. | [required] |
**submission_id** | **String** | The `id` of one of the participant's `submissions`. | [required] |
**set_creator_spark_code_request** | [**SetCreatorSparkCodeRequest**](SetCreatorSparkCodeRequest.md) |  | [required] |

### Return type

[**models::SetCreatorSparkCode200Response**](setCreatorSparkCode_200_response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## start_creator_connect

> models::StartCreatorConnect200Response start_creator_connect(token, start_creator_connect_request)
Start connecting a creator account

Returns the URL that connects one of the creator's own social accounts, read-only, so their posts can be verified. Only the campaign's platforms are accepted.  `authUrl` opens the welcome screen in the campaign's brand, then the platform's sign-in.  The creator comes back to their participant page, or to the connect window's result screen when `windowUrl` is sent. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**token** | **String** | A participant token or an open invite token. A malformed token answers 404 like an unknown one. | [required] |
**start_creator_connect_request** | [**StartCreatorConnectRequest**](StartCreatorConnectRequest.md) |  | [required] |

### Return type

[**models::StartCreatorConnect200Response**](startCreatorConnect_200_response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## start_creator_payouts

> models::StartCreatorPayouts200Response start_creator_payouts(token, start_creator_payouts_request)
Start payout onboarding

For a campaign that pays through the Zernio treasury: creates the creator's payee on first use and returns a Stripe-hosted onboarding link where they enter identity and bank details. `country` is required the first time and cannot change afterwards. About 20 attempts per participant every 10 minutes. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**token** | **String** | A participant token or an open invite token. A malformed token answers 404 like an unknown one. | [required] |
**start_creator_payouts_request** | [**StartCreatorPayoutsRequest**](StartCreatorPayoutsRequest.md) |  | [required] |

### Return type

[**models::StartCreatorPayouts200Response**](startCreatorPayouts_200_response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## submit_creator_draft

> models::SubmitCreatorDraft201Response submit_creator_draft(token, submit_creator_draft_request)
Submit a draft for review

Sends a draft for the campaign team to review before the creator publishes, on a campaign with `requireDraftApproval`, and fires `campaign_draft.submitted`. `mediaUrl` must be a `publicUrl` from `POST /public/creator-campaigns/{token}/drafts/upload`.  ### Revisions  - Without `revisionOf` the draft starts a new chain at version 1. - With `revisionOf` it is the next version of that chain. Only one of the creator's own versions marked `revision_requested` takes a new version, and only once.  About 20 drafts per participant every 10 minutes. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**token** | **String** | A participant token or an open invite token. A malformed token answers 404 like an unknown one. | [required] |
**submit_creator_draft_request** | [**SubmitCreatorDraftRequest**](SubmitCreatorDraftRequest.md) |  | [required] |

### Return type

[**models::SubmitCreatorDraft201Response**](submitCreatorDraft_201_response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## submit_creator_post

> models::SubmitCreatorPost201Response submit_creator_post(token, submit_creator_post_request)
Submit a post

Submits the link to a post the creator published from a connected account. The post opens a tracking window and fires `campaign_submission.received` to the operator. About 30 attempts and 10 accepted posts per participant every 10 minutes. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**token** | **String** | A participant token or an open invite token. A malformed token answers 404 like an unknown one. | [required] |
**submit_creator_post_request** | [**SubmitCreatorPostRequest**](SubmitCreatorPostRequest.md) |  | [required] |

### Return type

[**models::SubmitCreatorPost201Response**](submitCreatorPost_201_response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

