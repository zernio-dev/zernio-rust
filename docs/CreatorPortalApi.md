# \CreatorPortalApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_creator_payout_login**](CreatorPortalApi.md#create_creator_payout_login) | **POST** /public/creator-campaigns/{token}/payout-login | Open the creator's Stripe dashboard
[**get_creator_payout_statement**](CreatorPortalApi.md#get_creator_payout_statement) | **GET** /public/creator-campaigns/{token}/payouts/{transferId}/statement | Download a payout statement
[**get_creator_payouts**](CreatorPortalApi.md#get_creator_payouts) | **GET** /public/creator-campaigns/{token}/payouts | List a creator's earnings history
[**get_creator_portal**](CreatorPortalApi.md#get_creator_portal) | **GET** /public/creator-campaigns/{token} | Read a creator invite or participant page
[**join_creator_campaign**](CreatorPortalApi.md#join_creator_campaign) | **POST** /public/creator-campaigns/{token} | Join a campaign
[**recover_creator_portal_links**](CreatorPortalApi.md#recover_creator_portal_links) | **POST** /public/creator-campaigns/recover-link | Email a creator their campaign links
[**start_creator_connect**](CreatorPortalApi.md#start_creator_connect) | **POST** /public/creator-campaigns/{token}/connect | Start connecting a creator account
[**start_creator_payouts**](CreatorPortalApi.md#start_creator_payouts) | **POST** /public/creator-campaigns/{token}/payouts | Start payout onboarding
[**submit_creator_post**](CreatorPortalApi.md#submit_creator_post) | **POST** /public/creator-campaigns/{token}/submissions | Submit a post



## create_creator_payout_login

> models::StartCreatorPayouts200Response create_creator_payout_login(token)
Open the creator's Stripe dashboard

Returns a one-time link into the creator's Stripe Express dashboard, where they change bank details and see each payout. Only after the creator submitted their payout details. About 20 attempts per participant every 10 minutes. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**token** | **String** | A participant token or an open invite token. A malformed token answers 404 like an unknown one. | [required] |

### Return type

[**models::StartCreatorPayouts200Response**](startCreatorPayouts_200_response.md)

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

What a creator sees behind a campaign link, with no API key. Never cached.  `token` is one of:  - An open invite token (from `POST /v1/creator-campaigns/{campaignId}/invite-link`): answers `kind: invite` with the campaign only. - A participant token (from an invite or a join): answers `kind: participant` with the creator's connected accounts, latest 100 submissions, earnings and payout setup.  Reading a participant page also re-checks the creator's connected accounts. 

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

Accepts a participant invite, or joins through an open invite link.  - Participant token: the body is ignored and the invite is accepted. - Open invite token: a new participant is created from `displayName` (required) and `email` (optional), and a fresh participant token comes back. Keep it: it is the creator's only key to their page.  Open-link joins are limited to about 20 per IP address and 60 per link every 10 minutes. 

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


## start_creator_connect

> models::StartCreatorConnect200Response start_creator_connect(token, start_creator_connect_request)
Start connecting a creator account

Returns the authorization URL that connects one of the creator's own social accounts, read-only, so their posts can be verified. Send the creator's browser to `authUrl`; they come back to their participant page. Only the campaign's platforms are accepted. 

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

