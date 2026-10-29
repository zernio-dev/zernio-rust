# \CreatorCampaignsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**activate_creator_campaign**](CreatorCampaignsApi.md#activate_creator_campaign) | **POST** /v1/creator-campaigns/{campaignId}/activate | Activate creator campaign
[**approve_campaign_submission**](CreatorCampaignsApi.md#approve_campaign_submission) | **POST** /v1/creator-campaigns/{campaignId}/submissions/{submissionId}/approve | Approve campaign submission
[**close_creator_campaign**](CreatorCampaignsApi.md#close_creator_campaign) | **POST** /v1/creator-campaigns/{campaignId}/close | Close creator campaign
[**create_campaign_adjustment**](CreatorCampaignsApi.md#create_campaign_adjustment) | **POST** /v1/creator-campaigns/{campaignId}/adjustments | Create campaign adjustment
[**create_campaign_invite_link**](CreatorCampaignsApi.md#create_campaign_invite_link) | **POST** /v1/creator-campaigns/{campaignId}/invite-link | Create campaign invite link
[**create_campaign_participant**](CreatorCampaignsApi.md#create_campaign_participant) | **POST** /v1/creator-campaigns/{campaignId}/participants | Invite campaign participant
[**create_campaign_payout_batch**](CreatorCampaignsApi.md#create_campaign_payout_batch) | **POST** /v1/creator-campaigns/{campaignId}/payout-batches | Pay creators with one card payment
[**create_creator_campaign**](CreatorCampaignsApi.md#create_creator_campaign) | **POST** /v1/creator-campaigns | Create creator campaign
[**get_campaign_participant**](CreatorCampaignsApi.md#get_campaign_participant) | **GET** /v1/creator-campaigns/{campaignId}/participants/{participantId} | Get campaign participant
[**get_campaign_report**](CreatorCampaignsApi.md#get_campaign_report) | **GET** /v1/creator-campaigns/{campaignId}/report | Get campaign report
[**get_campaign_submission**](CreatorCampaignsApi.md#get_campaign_submission) | **GET** /v1/creator-campaigns/{campaignId}/submissions/{submissionId} | Get campaign submission
[**get_creator_campaign**](CreatorCampaignsApi.md#get_creator_campaign) | **GET** /v1/creator-campaigns/{campaignId} | Get creator campaign
[**list_campaign_ledger**](CreatorCampaignsApi.md#list_campaign_ledger) | **GET** /v1/creator-campaigns/{campaignId}/ledger | List campaign ledger
[**list_campaign_participants**](CreatorCampaignsApi.md#list_campaign_participants) | **GET** /v1/creator-campaigns/{campaignId}/participants | List campaign participants
[**list_campaign_payables**](CreatorCampaignsApi.md#list_campaign_payables) | **GET** /v1/creator-campaigns/{campaignId}/payables | List campaign payables
[**list_campaign_payout_batches**](CreatorCampaignsApi.md#list_campaign_payout_batches) | **GET** /v1/creator-campaigns/{campaignId}/payout-batches | List payout batches
[**list_campaign_submissions**](CreatorCampaignsApi.md#list_campaign_submissions) | **GET** /v1/creator-campaigns/{campaignId}/submissions | List campaign submissions
[**list_creator_campaigns**](CreatorCampaignsApi.md#list_creator_campaigns) | **GET** /v1/creator-campaigns | List creator campaigns
[**pause_creator_campaign**](CreatorCampaignsApi.md#pause_creator_campaign) | **POST** /v1/creator-campaigns/{campaignId}/pause | Pause creator campaign
[**raise_creator_campaign_budget**](CreatorCampaignsApi.md#raise_creator_campaign_budget) | **POST** /v1/creator-campaigns/{campaignId}/budget | Raise creator campaign budget
[**reinstate_campaign_participant**](CreatorCampaignsApi.md#reinstate_campaign_participant) | **POST** /v1/creator-campaigns/{campaignId}/participants/{participantId}/reinstate | Reinstate campaign participant
[**reject_campaign_submission**](CreatorCampaignsApi.md#reject_campaign_submission) | **POST** /v1/creator-campaigns/{campaignId}/submissions/{submissionId}/reject | Reject campaign submission
[**remove_campaign_participant**](CreatorCampaignsApi.md#remove_campaign_participant) | **POST** /v1/creator-campaigns/{campaignId}/participants/{participantId}/remove | Remove campaign participant
[**reopen_campaign_submission**](CreatorCampaignsApi.md#reopen_campaign_submission) | **POST** /v1/creator-campaigns/{campaignId}/submissions/{submissionId}/reopen | Reopen campaign submission
[**settle_campaign_participant**](CreatorCampaignsApi.md#settle_campaign_participant) | **POST** /v1/creator-campaigns/{campaignId}/participants/{participantId}/settle | Settle campaign participant
[**suspend_campaign_participant**](CreatorCampaignsApi.md#suspend_campaign_participant) | **POST** /v1/creator-campaigns/{campaignId}/participants/{participantId}/suspend | Suspend campaign participant
[**update_creator_campaign**](CreatorCampaignsApi.md#update_creator_campaign) | **PATCH** /v1/creator-campaigns/{campaignId} | Update creator campaign



## activate_creator_campaign

> models::CreateCreatorCampaign201Response activate_creator_campaign(campaign_id)
Activate creator campaign

Moves a `draft` or `paused` campaign to `active`, where creators can join and submit posts and tracked views accrue earnings. Needs at least one platform and a budget above zero; any other starting state answers 409. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |

### Return type

[**models::CreateCreatorCampaign201Response**](createCreatorCampaign_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## approve_campaign_submission

> models::ApproveCampaignSubmission200Response approve_campaign_submission(campaign_id, submission_id, idempotency_key)
Approve campaign submission

Approves a `tracking` or `pending_review` submission of an active campaign and fires `campaign_submission.approved`.  The Zernio dashboard offers Approve only on `pending_review` (a post that needs a decision) and waits for `tracking` posts to get there. The API accepts `tracking` so an integration can approve early.  ### Earnings  - What the post earned so far moves to owed and is held for the campaign's `holdDays`. - Later earnings post straight to owed. - A per-post campaign pays `perApprovedPostCents` here.  ### Errors  - 409: the submission is in any other state. - 409 (`invalid_resource_state`, \"This post is already approved in another campaign of yours.\"): the same post was approved in another of your campaigns, so one post never earns twice. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**submission_id** | **String** | Submission ID. | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  |  |

### Return type

[**models::ApproveCampaignSubmission200Response**](approveCampaignSubmission_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## close_creator_campaign

> models::CreateCreatorCampaign201Response close_creator_campaign(campaign_id)
Close creator campaign

Closes an `active` or `paused` campaign for good and fires `creator_campaign.closed`. Open tracking windows are cancelled.  A pool campaign is split among participants at this moment by their approved eligible views. Closing a pool campaign therefore answers 409 while any post still awaits review.  A campaign also closes by itself once `endsAt` passed and every tracking window had its final read. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |

### Return type

[**models::CreateCreatorCampaign201Response**](createCreatorCampaign_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_campaign_adjustment

> models::CreateCampaignAdjustment201Response create_campaign_adjustment(campaign_id, create_campaign_adjustment_request, idempotency_key)
Create campaign adjustment

Posts a manual adjustment to a participant's payable balance against the campaign budget: a positive amount credits the participant (a bonus), a negative one claws back. `cause` is kept on the ledger entry. A claw-back larger than the payable balance answers 409. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**create_campaign_adjustment_request** | [**CreateCampaignAdjustmentRequest**](CreateCampaignAdjustmentRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  |  |

### Return type

[**models::CreateCampaignAdjustment201Response**](createCampaignAdjustment_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_campaign_invite_link

> models::CreateCampaignInviteLink201Response create_campaign_invite_link(campaign_id)
Create campaign invite link

Creates the campaign's open invite link: anyone with it can join as a participant (up to `caps.maxParticipants`). Creating a new link revokes the previous one. The URL is returned only here. Answers 409 on a closed campaign. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |

### Return type

[**models::CreateCampaignInviteLink201Response**](createCampaignInviteLink_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_campaign_participant

> models::CreateCampaignParticipant201Response create_campaign_participant(campaign_id, create_campaign_participant_request, idempotency_key)
Invite campaign participant

Invites one creator and returns their personal invite URL.  Send the URL to the creator. On that page they connect their accounts (read-only), submit posts and see their earnings.  ### Invite rules  - The URL is returned only here; inviting again creates no second link. - A creator is matched by email within your workspace, so the same person keeps one identity across your campaigns.  ### Errors  - 409: the creator is already in the campaign, or the campaign is closed. - 403 `feature_not_available`: `caps.maxParticipants` is reached. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**create_campaign_participant_request** | [**CreateCampaignParticipantRequest**](CreateCampaignParticipantRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  |  |

### Return type

[**models::CreateCampaignParticipant201Response**](createCampaignParticipant_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_campaign_payout_batch

> models::CreateCampaignPayoutBatch201Response create_campaign_payout_batch(campaign_id, idempotency_key, create_campaign_payout_batch_request)
Pay creators with one card payment

Pays exactly what is owed to the creators of a `treasury` campaign, through one Stripe Checkout card payment.  ### How it works  1. Every payable creator who finished payout setup (or only `participantIds`, minus `excludeParticipantIds`) is held in `settling`. 2. The response carries a Stripe Checkout `url` for the total plus the fee (4% per creator, 50 cent minimum). 3. Once the card payment completes, each creator gets a transfer funded by that charge, and the batch ends `paid` or `partially_failed`.  A creator whose payouts were disabled before the payment landed is skipped and stays payable. If the Checkout expires unpaid (24 hours), every amount is payable again.  ### Limits and errors  - 402: card payouts are limited to $2,000.00 gross per rolling 30 days by default. Over it the call answers \"Over your instant payout limit. Top up your balance to pay more this month, or contact support to raise the limit.\" - 400: nothing payable (\"Nothing is payable.\").  ### Access and retries  Needs an owner, admin or billing admin, signed in or through a full-access key they created.  Send an `Idempotency-Key` so a retry never opens a second batch. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  |  |
**create_campaign_payout_batch_request** | Option<[**CreateCampaignPayoutBatchRequest**](CreateCampaignPayoutBatchRequest.md)> |  |  |

### Return type

[**models::CreateCampaignPayoutBatch201Response**](createCampaignPayoutBatch_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_creator_campaign

> models::CreateCreatorCampaign201Response create_creator_campaign(create_creator_campaign_request, idempotency_key)
Create creator campaign

Creates a campaign in `draft`. Creators are paid for verified performance of the posts they submit: Zernio tracks each post through a tracking window, scores its authenticity and records every earning in a ledger. Activate the campaign to start accepting submissions.  Creator campaigns run on usage-based billing; a workspace not on it gets 403 `feature_not_available`. `profileId` must be a profile this key can reach, otherwise 404. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_creator_campaign_request** | [**CreateCreatorCampaignRequest**](CreateCreatorCampaignRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  |  |

### Return type

[**models::CreateCreatorCampaign201Response**](createCreatorCampaign_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_campaign_participant

> models::GetCampaignParticipant200Response get_campaign_participant(campaign_id, participant_id)
Get campaign participant

Returns one participant with connected accounts, balances by state, flags and submission counts. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**participant_id** | **String** | Participant ID. | [required] |

### Return type

[**models::GetCampaignParticipant200Response**](getCampaignParticipant_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_campaign_report

> models::GetCampaignReport200Response get_campaign_report(campaign_id)
Get campaign report

Returns spend against budget, views, submission counts, the top ten participants by earnings and the authenticity score distribution. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |

### Return type

[**models::GetCampaignReport200Response**](getCampaignReport_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_campaign_submission

> models::GetCampaignSubmission200Response get_campaign_submission(campaign_id, submission_id)
Get campaign submission

Returns one submission with its per-sync samples (views, likes, comments, shares, saves). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**submission_id** | **String** | Submission ID. | [required] |

### Return type

[**models::GetCampaignSubmission200Response**](getCampaignSubmission_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_creator_campaign

> models::CreateCreatorCampaign201Response get_creator_campaign(campaign_id)
Get creator campaign

Returns the campaign with its budget consumption, participant count and submission counts. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |

### Return type

[**models::CreateCreatorCampaign201Response**](createCreatorCampaign_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_campaign_ledger

> models::ListCampaignLedger200Response list_campaign_ledger(campaign_id, participant_id, kind, limit, skip)
List campaign ledger

Lists ledger entries, newest first.  Without `participantId` it lists every entry of the campaign:  - earnings drawn from the budget (accruals, per-post payments, pool shares, adjustments) - the approvals, hold releases and settlements that move money between its participants' buckets - their reversals  Pass `participantId` to narrow the list to one participant's entries. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**participant_id** | Option<**String**> | List only this participant's entries. |  |
**kind** | Option<**String**> |  |  |
**limit** | Option<**i32**> |  |  |[default to 50]
**skip** | Option<**i32**> |  |  |[default to 0]

### Return type

[**models::ListCampaignLedger200Response**](listCampaignLedger_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_campaign_participants

> models::ListCampaignParticipants200Response list_campaign_participants(campaign_id, status, limit, skip)
List campaign participants

Lists the campaign's participants with their balances, flags and submission counts. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**status** | Option<**String**> |  |  |
**limit** | Option<**i32**> |  |  |[default to 50]
**skip** | Option<**i32**> |  |  |[default to 0]

### Return type

[**models::ListCampaignParticipants200Response**](listCampaignParticipants_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_campaign_payables

> models::ListCampaignPayables200Response list_campaign_payables(campaign_id)
List campaign payables

Lists every participant with a payable balance (earnings past their hold), with the ledger entries behind it. Pay these, then record each payout with the settle endpoint. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |

### Return type

[**models::ListCampaignPayables200Response**](listCampaignPayables_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_campaign_payout_batches

> models::ListCampaignPayoutBatches200Response list_campaign_payout_batches(campaign_id, limit, skip)
List payout batches

The campaign's payout batches, newest first, with each creator's item.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**limit** | Option<**i32**> |  |  |[default to 20]
**skip** | Option<**i32**> |  |  |[default to 0]

### Return type

[**models::ListCampaignPayoutBatches200Response**](listCampaignPayoutBatches_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_campaign_submissions

> models::ListCampaignSubmissions200Response list_campaign_submissions(campaign_id, status, participant_id, flag, platform, min_score, max_score, q, sort, order, limit, skip)
List campaign submissions

Lists submitted posts with views, earnings, authenticity score and flags. Filter by status, participant, flag, platform or score range to build a review queue, for example `status=pending_review`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**status** | Option<**String**> |  |  |
**participant_id** | Option<**String**> |  |  |
**flag** | Option<**String**> |  |  |
**platform** | Option<**String**> |  |  |
**min_score** | Option<**i32**> |  |  |
**max_score** | Option<**i32**> |  |  |
**q** | Option<**String**> | Only submissions whose creator name or post link contains this text, ignoring case. |  |
**sort** | Option<**String**> | What to sort by. Posts with no value to sort by (not read yet, not scored) come last in either direction. |  |[default to submittedAt]
**order** | Option<**String**> |  |  |[default to desc]
**limit** | Option<**i32**> |  |  |[default to 50]
**skip** | Option<**i32**> |  |  |[default to 0]

### Return type

[**models::ListCampaignSubmissions200Response**](listCampaignSubmissions_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_creator_campaigns

> models::ListCreatorCampaigns200Response list_creator_campaigns(status, profile_id, q, limit, skip)
List creator campaigns

Lists the team's campaigns in the profiles this key can reach, newest first. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**status** | Option<**String**> |  |  |
**profile_id** | Option<**String**> | Only campaigns in this profile. |  |
**q** | Option<**String**> | Only campaigns whose name or brand name contains this text, ignoring case. |  |
**limit** | Option<**i32**> |  |  |[default to 50]
**skip** | Option<**i32**> |  |  |[default to 0]

### Return type

[**models::ListCreatorCampaigns200Response**](listCreatorCampaigns_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## pause_creator_campaign

> models::CreateCreatorCampaign201Response pause_creator_campaign(campaign_id)
Pause creator campaign

Moves an `active` campaign to `paused`: no new submissions, and approvals answer 409 until the campaign is activated again. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |

### Return type

[**models::CreateCreatorCampaign201Response**](createCreatorCampaign_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## raise_creator_campaign_budget

> models::CreateCreatorCampaign201Response raise_creator_campaign_budget(campaign_id, raise_creator_campaign_budget_request, idempotency_key)
Raise creator campaign budget

Raises the budget of a campaign that is `draft`, `active` or `paused`.  Only the budget changes. The pay terms stay as creators joined them, which `PATCH` refuses to change once the campaign is live.  - The new `budgetCents` must be above the current budget, otherwise 400 `invalid_field_value`. - When it is also above what the campaign has spent, `budgetExhaustedAt` is cleared and earnings that stopped at the old budget resume. - A closed campaign answers 409 `invalid_resource_state`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**raise_creator_campaign_budget_request** | [**RaiseCreatorCampaignBudgetRequest**](RaiseCreatorCampaignBudgetRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  |  |

### Return type

[**models::CreateCreatorCampaign201Response**](createCreatorCampaign_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reinstate_campaign_participant

> models::GetCampaignParticipant200Response reinstate_campaign_participant(campaign_id, participant_id)
Reinstate campaign participant

Reinstates a `suspended` participant: they can submit posts again. Any other status answers 409; a removed participant stays removed. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**participant_id** | **String** | Participant ID. | [required] |

### Return type

[**models::GetCampaignParticipant200Response**](getCampaignParticipant_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reject_campaign_submission

> models::ApproveCampaignSubmission200Response reject_campaign_submission(campaign_id, submission_id, reject_campaign_submission_request, idempotency_key)
Reject campaign submission

Rejects a submission (also one already approved) and fires `campaign_submission.rejected`. Its tracking window is cancelled and its unsettled earnings return to the campaign budget. Rejecting a rejected submission returns it unchanged; an expired or withdrawn one answers 409. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**submission_id** | **String** | Submission ID. | [required] |
**reject_campaign_submission_request** | [**RejectCampaignSubmissionRequest**](RejectCampaignSubmissionRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  |  |

### Return type

[**models::ApproveCampaignSubmission200Response**](approveCampaignSubmission_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_campaign_participant

> models::GetCampaignParticipant200Response remove_campaign_participant(campaign_id, participant_id)
Remove campaign participant

Removes the participant from the campaign. Their earnings stay in the ledger. Removing an already removed participant returns it unchanged. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**participant_id** | **String** | Participant ID. | [required] |

### Return type

[**models::GetCampaignParticipant200Response**](getCampaignParticipant_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reopen_campaign_submission

> models::ApproveCampaignSubmission200Response reopen_campaign_submission(campaign_id, submission_id, idempotency_key)
Reopen campaign submission

Puts a rejected submission back to `pending_review` so it can be decided again. No webhook fires.  Its tracking window resumes, so it works only while that window has not ended.  ### When it can't be reopened  - The tracking window has ended: 409 `invalid_resource_state` (\"This post's tracking window has ended.\"). - A post that earned money which was already paid out cannot be reopened. - A post of a closed campaign cannot be reopened. - Any status other than rejected or `pending_review` answers 409.  Reopening a submission that is already `pending_review` returns it unchanged. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**submission_id** | **String** | Submission ID. | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  |  |

### Return type

[**models::ApproveCampaignSubmission200Response**](approveCampaignSubmission_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## settle_campaign_participant

> models::SettleCampaignParticipant201Response settle_campaign_participant(campaign_id, participant_id, settle_campaign_participant_request, idempotency_key)
Settle campaign participant

Records a payout of the participant's payable balance and fires `campaign_payout.settled`.  Omit `amountCents` to settle the whole payable balance. An amount above it answers 400, and nothing payable answers 409. Send an `Idempotency-Key` so a retry never records the payout twice.  ### Settlement modes  - `none` settlement: records a payout you made elsewhere. - `external` settlement: pay from your own rails when `campaign_payout.payable` fires, then call this with your payout id in `externalReference` (required in this mode). - `treasury` settlement: transfers the amount from your Zernio balance to the creator's connected Stripe account, then records it with the Stripe transfer id as `externalReference`.  ### Treasury payouts  The transfer fee (4%, $0.50 minimum) is added on top: the creator receives the full amount and your balance is debited `totalCents`.  - The creator must have finished payout setup from their campaign page (409 otherwise). - A balance that does not cover the amount plus the fee answers 402.  Set `recordOnly: true` to record a payout you made yourself instead of moving money through the treasury (the webhook then carries `recorded: true`).  A treasury payout needs an owner, admin or billing admin, signed in or through a full-access key they created (403 otherwise). Recording with `recordOnly` does not.  #### While Stripe confirms the transfer  The amount sits in the participant's `settling` balance; a reject in that window cannot reverse it.  - If Stripe refuses the transfer, the amount returns to payable. - If Stripe does not answer, the amount stays in `settling`. The next settle call for this participant finishes that payout first (even with nothing payable left).  #### Conflicts (409)  - A retry asking for a different `amountCents` than the payout in progress answers 409 with the amount in progress. - A settle while another request is still waiting on Stripe for the same payout answers 409 (\"This payout is being sent to Stripe right now. Try again in a minute.\"). - A payout Stripe has not confirmed after 24 hours answers 409 (\"This payout is being confirmed with Stripe. Try again after the next reconciliation (within 24 hours).\") until the daily reconciliation finishes it: settled if Stripe made the transfer, returned to payable if it did not. - A creator held by an unfinished payout batch answers 409 (\"This creator is in a card payout that is not finished yet.\"). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**participant_id** | **String** | Participant ID. | [required] |
**settle_campaign_participant_request** | [**SettleCampaignParticipantRequest**](SettleCampaignParticipantRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  |  |

### Return type

[**models::SettleCampaignParticipant201Response**](settleCampaignParticipant_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## suspend_campaign_participant

> models::GetCampaignParticipant200Response suspend_campaign_participant(campaign_id, participant_id)
Suspend campaign participant

Suspends an `active` participant: they can no longer submit posts. Any other status answers 409. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**participant_id** | **String** | Participant ID. | [required] |

### Return type

[**models::GetCampaignParticipant200Response**](getCampaignParticipant_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_creator_campaign

> models::CreateCreatorCampaign201Response update_creator_campaign(campaign_id, update_creator_campaign_request)
Update creator campaign

Updates any subset of the campaign's settings. `economics` (and with it the campaign type) can only change while the campaign is a draft; afterwards that answers 409, and a live campaign's budget is raised with `POST /v1/creator-campaigns/{campaignId}/budget`. An empty body answers 400. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**update_creator_campaign_request** | [**UpdateCreatorCampaignRequest**](UpdateCreatorCampaignRequest.md) |  | [required] |

### Return type

[**models::CreateCreatorCampaign201Response**](createCreatorCampaign_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

