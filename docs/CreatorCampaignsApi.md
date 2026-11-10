# \CreatorCampaignsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**activate_creator_campaign**](CreatorCampaignsApi.md#activate_creator_campaign) | **POST** /v1/creator-campaigns/{campaignId}/activate | Activate creator campaign
[**approve_campaign_draft**](CreatorCampaignsApi.md#approve_campaign_draft) | **POST** /v1/creator-campaigns/{campaignId}/drafts/{draftId}/approve | Approve campaign draft
[**approve_campaign_participant**](CreatorCampaignsApi.md#approve_campaign_participant) | **POST** /v1/creator-campaigns/{campaignId}/participants/{participantId}/approve | Approve pending campaign participant
[**approve_campaign_sample**](CreatorCampaignsApi.md#approve_campaign_sample) | **POST** /v1/creator-campaigns/{campaignId}/samples/{sampleId}/approve | Approve campaign sample request
[**approve_campaign_submission**](CreatorCampaignsApi.md#approve_campaign_submission) | **POST** /v1/creator-campaigns/{campaignId}/submissions/{submissionId}/approve | Approve campaign submission
[**close_creator_campaign**](CreatorCampaignsApi.md#close_creator_campaign) | **POST** /v1/creator-campaigns/{campaignId}/close | Close creator campaign
[**create_campaign_adjustment**](CreatorCampaignsApi.md#create_campaign_adjustment) | **POST** /v1/creator-campaigns/{campaignId}/adjustments | Create campaign adjustment
[**create_campaign_invite_link**](CreatorCampaignsApi.md#create_campaign_invite_link) | **POST** /v1/creator-campaigns/{campaignId}/invite-link | Create campaign invite link
[**create_campaign_participant**](CreatorCampaignsApi.md#create_campaign_participant) | **POST** /v1/creator-campaigns/{campaignId}/participants | Invite campaign participant
[**create_campaign_payout_batch**](CreatorCampaignsApi.md#create_campaign_payout_batch) | **POST** /v1/creator-campaigns/{campaignId}/payout-batches | Pay creators with one card payment
[**create_creator_campaign**](CreatorCampaignsApi.md#create_creator_campaign) | **POST** /v1/creator-campaigns | Create creator campaign
[**decline_campaign_sample**](CreatorCampaignsApi.md#decline_campaign_sample) | **POST** /v1/creator-campaigns/{campaignId}/samples/{sampleId}/decline | Decline campaign sample request
[**deny_campaign_participant**](CreatorCampaignsApi.md#deny_campaign_participant) | **POST** /v1/creator-campaigns/{campaignId}/participants/{participantId}/deny | Deny pending campaign participant
[**get_campaign_ad_results**](CreatorCampaignsApi.md#get_campaign_ad_results) | **GET** /v1/creator-campaigns/{campaignId}/ad-results | Get campaign ad results
[**get_campaign_draft**](CreatorCampaignsApi.md#get_campaign_draft) | **GET** /v1/creator-campaigns/{campaignId}/drafts/{draftId} | Get campaign draft
[**get_campaign_participant**](CreatorCampaignsApi.md#get_campaign_participant) | **GET** /v1/creator-campaigns/{campaignId}/participants/{participantId} | Get campaign participant
[**get_campaign_report**](CreatorCampaignsApi.md#get_campaign_report) | **GET** /v1/creator-campaigns/{campaignId}/report | Get campaign report
[**get_campaign_submission**](CreatorCampaignsApi.md#get_campaign_submission) | **GET** /v1/creator-campaigns/{campaignId}/submissions/{submissionId} | Get campaign submission
[**get_creator_campaign**](CreatorCampaignsApi.md#get_creator_campaign) | **GET** /v1/creator-campaigns/{campaignId} | Get creator campaign
[**launch_campaign_ads**](CreatorCampaignsApi.md#launch_campaign_ads) | **POST** /v1/creator-campaigns/{campaignId}/ads/launch | Launch campaign posts as ads
[**list_campaign_drafts**](CreatorCampaignsApi.md#list_campaign_drafts) | **GET** /v1/creator-campaigns/{campaignId}/drafts | List campaign drafts
[**list_campaign_ledger**](CreatorCampaignsApi.md#list_campaign_ledger) | **GET** /v1/creator-campaigns/{campaignId}/ledger | List campaign ledger
[**list_campaign_orders**](CreatorCampaignsApi.md#list_campaign_orders) | **GET** /v1/creator-campaigns/{campaignId}/orders | List campaign orders
[**list_campaign_participants**](CreatorCampaignsApi.md#list_campaign_participants) | **GET** /v1/creator-campaigns/{campaignId}/participants | List campaign participants
[**list_campaign_payables**](CreatorCampaignsApi.md#list_campaign_payables) | **GET** /v1/creator-campaigns/{campaignId}/payables | List campaign payables
[**list_campaign_payout_batches**](CreatorCampaignsApi.md#list_campaign_payout_batches) | **GET** /v1/creator-campaigns/{campaignId}/payout-batches | List payout batches
[**list_campaign_samples**](CreatorCampaignsApi.md#list_campaign_samples) | **GET** /v1/creator-campaigns/{campaignId}/samples | List campaign sample requests
[**list_campaign_submissions**](CreatorCampaignsApi.md#list_campaign_submissions) | **GET** /v1/creator-campaigns/{campaignId}/submissions | List campaign submissions
[**list_creator_campaigns**](CreatorCampaignsApi.md#list_creator_campaigns) | **GET** /v1/creator-campaigns | List creator campaigns
[**move_campaign_participant**](CreatorCampaignsApi.md#move_campaign_participant) | **POST** /v1/creator-campaigns/{campaignId}/participants/{participantId}/move | Move participant to another campaign
[**pause_creator_campaign**](CreatorCampaignsApi.md#pause_creator_campaign) | **POST** /v1/creator-campaigns/{campaignId}/pause | Pause creator campaign
[**preview_campaign_payout_batch**](CreatorCampaignsApi.md#preview_campaign_payout_batch) | **POST** /v1/creator-campaigns/{campaignId}/payout-batches/preview | Preview a payout batch
[**raise_creator_campaign_budget**](CreatorCampaignsApi.md#raise_creator_campaign_budget) | **POST** /v1/creator-campaigns/{campaignId}/budget | Raise creator campaign budget
[**reinstate_campaign_participant**](CreatorCampaignsApi.md#reinstate_campaign_participant) | **POST** /v1/creator-campaigns/{campaignId}/participants/{participantId}/reinstate | Reinstate campaign participant
[**reject_campaign_draft**](CreatorCampaignsApi.md#reject_campaign_draft) | **POST** /v1/creator-campaigns/{campaignId}/drafts/{draftId}/reject | Reject campaign draft
[**reject_campaign_submission**](CreatorCampaignsApi.md#reject_campaign_submission) | **POST** /v1/creator-campaigns/{campaignId}/submissions/{submissionId}/reject | Reject campaign submission
[**remove_campaign_participant**](CreatorCampaignsApi.md#remove_campaign_participant) | **POST** /v1/creator-campaigns/{campaignId}/participants/{participantId}/remove | Remove campaign participant
[**reopen_campaign_submission**](CreatorCampaignsApi.md#reopen_campaign_submission) | **POST** /v1/creator-campaigns/{campaignId}/submissions/{submissionId}/reopen | Reopen campaign submission
[**request_campaign_draft_revision**](CreatorCampaignsApi.md#request_campaign_draft_revision) | **POST** /v1/creator-campaigns/{campaignId}/drafts/{draftId}/request-revision | Request changes on a campaign draft
[**resend_campaign_participant_invite**](CreatorCampaignsApi.md#resend_campaign_participant_invite) | **POST** /v1/creator-campaigns/{campaignId}/participants/{participantId}/resend-invite | Resend campaign participant invite
[**settle_campaign_participant**](CreatorCampaignsApi.md#settle_campaign_participant) | **POST** /v1/creator-campaigns/{campaignId}/participants/{participantId}/settle | Settle campaign participant
[**ship_campaign_sample**](CreatorCampaignsApi.md#ship_campaign_sample) | **POST** /v1/creator-campaigns/{campaignId}/samples/{sampleId}/ship | Mark campaign sample shipped
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


## approve_campaign_draft

> models::ApproveCampaignDraft200Response approve_campaign_draft(campaign_id, draft_id, idempotency_key)
Approve campaign draft

Approves a `submitted` draft version, emails the creator and fires `campaign_draft.approved`. The creator can then publish it and submit the live post with this `draftId`; each approved draft backs one post only.  Each version is decided once: a version that is no longer `submitted` answers 409. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**draft_id** | **String** | Draft version ID. | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  |  |

### Return type

[**models::ApproveCampaignDraft200Response**](approveCampaignDraft_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## approve_campaign_participant

> models::GetCampaignParticipant200Response approve_campaign_participant(campaign_id, participant_id, idempotency_key)
Approve pending campaign participant

Lets a `pending` creator into the campaign: they become `active`, `joinedAt` is set, the creator is emailed and `campaign_participant.approved` fires (not `campaign_participant.joined`).  A creator is `pending` when they joined through the open link of a campaign with `joinApproval: manual`. Personal invites are never held.  ### Creator limit  Pending creators do not count toward `caps.maxParticipants`; the limit is checked here instead. A full campaign refuses the approval with 403 `feature_not_available` and the creator stays `pending`.  ### Errors  - 403 `feature_not_available`: the campaign reached `caps.maxParticipants`. - 409 `invalid_resource_state`: the participant is not `pending`, or the campaign is closed. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**participant_id** | **String** | Participant ID. | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  |  |

### Return type

[**models::GetCampaignParticipant200Response**](getCampaignParticipant_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## approve_campaign_sample

> models::ApproveCampaignSample200Response approve_campaign_sample(campaign_id, sample_id, idempotency_key)
Approve campaign sample request

Approves a `pending` sample request. Zernio creates a 100%-off, single-use discount code (`SAMPLE-XXXXXXXX`) limited to the requested product in the campaign's store (Shopify or WooCommerce), returns it as `discountCode`, emails it to the creator and fires `campaign_sample.approved`. The creator redeems it at checkout.  The code is created before the request changes, so when the store refuses (missing discount permission, an unsupported store, a store error) its error is returned and the request stays `pending`. The approval also starts the `sampleContentDueDays` clock behind `contentDueAt` and `contentOwed`.  ### Errors  - 400 `platform_not_supported`: the store cannot create discounts. - 403: the store has not granted the permission discounts need. - 409 `invalid_resource_state`: the request is not `pending`. - 502 `platform_api_error`: the store is unavailable. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**sample_id** | **String** | Sample request ID. | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  |  |

### Return type

[**models::ApproveCampaignSample200Response**](approveCampaignSample_200_response.md)

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
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  |  |

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
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  |  |

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
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  |  |

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

Pays exactly what is owed to the creators of a `treasury` campaign by charging the billing owner's saved card, with no redirect. Payouts are never paid from your balance.  ### How it works  1. Every payable creator who finished payout setup (or only `participantIds`, minus `excludeParticipantIds`) is held in `settling`. 2. The saved card (the default one, or `paymentMethodId`) pays one invoice while the payer is present: the payouts, plus the fee (4%, 50 cents minimum per payout) and the VAT on the fee where it applies. 3. Card payments are held 7 days against chargebacks (`releasesAt`). Then each creator gets a transfer funded by the charge, and the batch ends `paid` or `partially_failed`.  Zernio collects the payouts and pays each creator on your behalf and in your name, so the payouts carry no VAT.  A creator whose payouts were disabled before the hold ended is skipped and stays payable. A charge refunded or disputed during the hold pays nobody: every amount is payable again.  Preview the charge with `POST /v1/creator-campaigns/{campaignId}/payout-batches/preview`.  ### 3D Secure  `payment.status: requires_action` means the bank asked the payer to confirm. Complete it with Stripe.js `handleNextAction({ clientSecret })`, then call `POST /v1/payout-batches/{batchId}/confirm`.  One left unfinished is cancelled after 30 minutes and every amount is payable again. Cancel it sooner with `POST /v1/payout-batches/{batchId}/cancel`.  ### Limits and errors  - 402 `payment_required`: no saved card. Nothing is held. - 402 `card_declined`: the bank's reason; every amount is payable again. - 402: card payouts are limited to $10,000.00 gross per rolling 30 days by default. Over it the call answers \"Over your instant payout limit for the last 30 days. Contact support to raise it.\" - 402: your balance is negative after a dispute or refund. - 400: nothing payable (\"Nothing is payable.\"). - 400 `invalid_billing_address`: Stripe cannot place your billing address, so it cannot tax the fee. Nothing is held. - 429 `payment_attempts_limited`: five card payments were declined in 24 hours. Nothing is held and nothing reaches the bank until `Retry-After` runs out.  ### Access and retries  Needs an owner, admin or billing admin, signed in or through a full-access key they created.  Send an `Idempotency-Key` so a retry never opens a second batch. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  |  |
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
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  |  |

### Return type

[**models::CreateCreatorCampaign201Response**](createCreatorCampaign_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## decline_campaign_sample

> models::ApproveCampaignSample200Response decline_campaign_sample(campaign_id, sample_id, decline_campaign_sample_request, idempotency_key)
Decline campaign sample request

Declines a `pending` sample request with a reason, emails the creator and fires `campaign_sample.declined`. The creator can ask for the same product again. Any other status answers 409. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**sample_id** | **String** | Sample request ID. | [required] |
**decline_campaign_sample_request** | [**DeclineCampaignSampleRequest**](DeclineCampaignSampleRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  |  |

### Return type

[**models::ApproveCampaignSample200Response**](approveCampaignSample_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## deny_campaign_participant

> models::GetCampaignParticipant200Response deny_campaign_participant(campaign_id, participant_id, idempotency_key)
Deny pending campaign participant

Turns a `pending` creator away: they become `denied`, the creator is emailed and `campaign_participant.denied` fires. A denied creator cannot submit posts, drafts or sample requests. Any status other than `pending` answers 409. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**participant_id** | **String** | Participant ID. | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  |  |

### Return type

[**models::GetCampaignParticipant200Response**](getCampaignParticipant_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_campaign_ad_results

> models::GetCampaignAdResults200Response get_campaign_ad_results(campaign_id, rank_by, from, to)
Get campaign ad results

What the campaign's posts did as ads: totals, each post with its ads and launches, and the creators ranked by `rankBy`.  An ad counts for a post when it was launched from the post, or when it runs the post (a boosted post, the Instagram media it shows, or a TikTok Spark item).  Figures come from the ads' daily metrics; money is in the campaign currency, and ads billed in another currency are left out of money figures. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**rank_by** | Option<**String**> | How `creators` is ranked. |  |[default to spend]
**from** | Option<**String**> | First day counted (YYYY-MM-DD, UTC). Omit to count from the first day of data. |  |
**to** | Option<**String**> | Last day counted (YYYY-MM-DD, UTC). Omit to count through the latest day of data. |  |

### Return type

[**models::GetCampaignAdResults200Response**](getCampaignAdResults_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_campaign_draft

> models::GetCampaignDraft200Response get_campaign_draft(campaign_id, draft_id)
Get campaign draft

Returns one draft version and every version of its chain (`versions`, newest first, including this one), each with its review comments. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**draft_id** | **String** | Draft version ID. | [required] |

### Return type

[**models::GetCampaignDraft200Response**](getCampaignDraft_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
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


## launch_campaign_ads

> models::LaunchCampaignAds200Response launch_campaign_ads(campaign_id, launch_campaign_ads_request, idempotency_key)
Launch campaign posts as ads

Runs approved posts of an active campaign as ads, each post on its own: a post that cannot run is reported in `results` and never stops the rest.  A post already launched (or launching) into the same placement is reported as `already_launched` or `in_progress` and never gets a second ad, so a retry is safe.  ### What each post becomes  - **Meta, `identity: brand`**: a new ad from the post media in the existing ad set `adSetId`, under the brand's Page. - **Meta, `identity: creator`**: a Partnership Ad of the Instagram post under the creator's handle. Partnership Ads are a limited release while Meta reviews the permission they need (`capabilities.partnershipAds` in `GET /v1/creator-campaigns/{campaignId}/ad-results`); without it these posts fail with a message to launch them with brand identity. Facebook posts only run with brand identity. - **TikTok** (`identity: creator` only): a Spark Ad of the creator's post in its own ad group with `dailyBudget`, inside the existing campaign `existingCampaignId`. Needs the Spark code the creator pasted on their campaign page (`hasSparkCode` on the submission).  One launch runs on one network: posts from the other network fail with a message to launch them separately. Needs ads access (403 `ads_addon_required`) and room in the managed ads allowance (403 `ads_allowance_exceeded`). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**launch_campaign_ads_request** | [**LaunchCampaignAdsRequest**](LaunchCampaignAdsRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  |  |

### Return type

[**models::LaunchCampaignAds200Response**](launchCampaignAds_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_campaign_drafts

> models::ListCampaignDrafts200Response list_campaign_drafts(campaign_id, status, participant_id, limit, skip)
List campaign drafts

Lists the drafts creators uploaded for review on a campaign with `requireDraftApproval`, newest first.  Each draft is a chain of versions: a revision is a new version in the same `chainId`. Only the latest version of each chain is listed, so `status` is the chain's current state and `total` counts chains. Earlier versions come with `GET /v1/creator-campaigns/{campaignId}/drafts/{draftId}`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**status** | Option<**String**> | Only drafts whose latest version is in this status. `submitted` is the review queue. |  |
**participant_id** | Option<**String**> | Only drafts of this participant. |  |
**limit** | Option<**i32**> |  |  |[default to 50]
**skip** | Option<**i32**> |  |  |[default to 0]

### Return type

[**models::ListCampaignDrafts200Response**](listCampaignDrafts_200_response.md)

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


## list_campaign_orders

> models::ListCampaignOrders200Response list_campaign_orders(campaign_id, participant_id, status, limit, skip)
List campaign orders

Lists the store orders a commission or smart retainer campaign credited to its creators, newest first, and every active creator's discount code and tracking link.  An order is `pending` while the store is still attributing it (Shopify does so for a few minutes after checkout), `matched` once it is credited to a creator and `unmatched` when it never was. Commission is approved `holdDays` after the order was placed. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**participant_id** | Option<**String**> | Only this creator's orders. |  |
**status** | Option<**String**> |  |  |
**limit** | Option<**i32**> |  |  |[default to 50]
**skip** | Option<**i32**> |  |  |[default to 0]

### Return type

[**models::ListCampaignOrders200Response**](listCampaignOrders_200_response.md)

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


## list_campaign_samples

> models::ListCampaignSamples200Response list_campaign_samples(campaign_id, status, participant_id, limit, skip)
List campaign sample requests

Lists the free product samples creators asked for, newest first. `contentOwed` marks an approved or shipped sample whose creator submitted no post in the `sampleContentDueDays` since the approval. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**status** | Option<**String**> | Only requests in this status. `pending` is the review queue. |  |
**participant_id** | Option<**String**> | Only requests of this participant. |  |
**limit** | Option<**i32**> |  |  |[default to 50]
**skip** | Option<**i32**> |  |  |[default to 0]

### Return type

[**models::ListCampaignSamples200Response**](listCampaignSamples_200_response.md)

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


## move_campaign_participant

> models::MoveCampaignParticipant200Response move_campaign_participant(campaign_id, participant_id, move_campaign_participant_request)
Move participant to another campaign

Moves a creator invited or joined into the wrong campaign to another campaign of the same owner. The participant keeps its id, status and portal link, which now opens the target.  Posts that fit the target (platform accepted, published after it started) move with it. Undecided posts that do not fit are rejected in this campaign with the reason; decided ones stay.  Answers 409 when the target is closed or full, the creator is already in it, the participant was removed, or any money touched the participation (ledger entries, a payout batch or a transfer). Money never moves between campaigns.  Fires `campaign_participant.removed` here and, for a creator who joined, `campaign_participant.joined` on the target. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign the participant is in now. | [required] |
**participant_id** | **String** | Participant ID. | [required] |
**move_campaign_participant_request** | [**MoveCampaignParticipantRequest**](MoveCampaignParticipantRequest.md) |  | [required] |

### Return type

[**models::MoveCampaignParticipant200Response**](moveCampaignParticipant_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
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


## preview_campaign_payout_batch

> models::PreviewCampaignPayoutBatch200Response preview_campaign_payout_batch(campaign_id, preview_campaign_payout_batch_request)
Preview a payout batch

What `POST /v1/creator-campaigns/{campaignId}/payout-batches` with the same body would charge your card now. Holds and charges nothing.  The payouts carry no VAT. `taxCents` is the VAT on Zernio's fee where it applies, from Stripe Tax for your billing address: 21% in Spain, your country's rate for EU consumers, reverse charged (`reverseCharge: true`, no VAT) for EU businesses whose VAT id VIES confirms, none outside the EU.  Creators who have not finished payout setup are left out, as paying would. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**preview_campaign_payout_batch_request** | [**PreviewCampaignPayoutBatchRequest**](PreviewCampaignPayoutBatchRequest.md) |  | [required] |

### Return type

[**models::PreviewCampaignPayoutBatch200Response**](previewCampaignPayoutBatch_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
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
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  |  |

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


## reject_campaign_draft

> models::ApproveCampaignDraft200Response reject_campaign_draft(campaign_id, draft_id, reject_campaign_draft_request, idempotency_key)
Reject campaign draft

Rejects a `submitted` draft version for good, emails the creator and fires `campaign_draft.rejected`. The reason is stored as `reviewNote`. A rejected draft takes no new version and backs no post.  Each version is decided once: a version that is no longer `submitted` answers 409. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**draft_id** | **String** | Draft version ID. | [required] |
**reject_campaign_draft_request** | [**RejectCampaignDraftRequest**](RejectCampaignDraftRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  |  |

### Return type

[**models::ApproveCampaignDraft200Response**](approveCampaignDraft_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
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
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  |  |

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

Removes the participant from the campaign. Their earnings stay in the ledger. Removing an `invited` participant revokes their invite: the link stops working. Removing an already removed participant returns it unchanged. 

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
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  |  |

### Return type

[**models::ApproveCampaignSubmission200Response**](approveCampaignSubmission_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## request_campaign_draft_revision

> models::ApproveCampaignDraft200Response request_campaign_draft_revision(campaign_id, draft_id, request_campaign_draft_revision_request, idempotency_key)
Request changes on a campaign draft

Marks a `submitted` draft version `revision_requested`, emails the creator and fires `campaign_draft.revision_requested`. The creator answers with one new version (`revisionOf` set to this version).  Send a `note`, at least one entry in `comments`, or both; neither answers 400 `missing_required_field`. A comment with `atMs` is pinned to that moment of the video.  Each version is decided once: a version that is no longer `submitted` answers 409. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**draft_id** | **String** | Draft version ID. | [required] |
**request_campaign_draft_revision_request** | [**RequestCampaignDraftRevisionRequest**](RequestCampaignDraftRevisionRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  |  |

### Return type

[**models::ApproveCampaignDraft200Response**](approveCampaignDraft_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## resend_campaign_participant_invite

> models::GetCampaignParticipant200Response resend_campaign_participant_invite(campaign_id, participant_id, idempotency_key)
Resend campaign participant invite

Emails an `invited` participant their personal invite link again. The link does not change, so a link you already sent keeps working. The email counts toward the daily invite email cap of your workspace.  Answers 409 when the participant has already joined, was suspended or removed, has no email, or the campaign is closed. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**participant_id** | **String** | Participant ID. | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  |  |

### Return type

[**models::GetCampaignParticipant200Response**](getCampaignParticipant_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## settle_campaign_participant

> models::SettleCampaignParticipant201Response settle_campaign_participant(campaign_id, participant_id, settle_campaign_participant_request, idempotency_key)
Settle campaign participant

Records a payout of the participant's payable balance and fires `campaign_payout.settled`. No money moves through Zernio.  Omit `amountCents` to settle the whole payable balance. An amount above it answers 400, and nothing payable answers 409. Send an `Idempotency-Key` so a retry never records the payout twice.  ### Settlement modes  - `none` settlement: records a payout you made elsewhere. - `external` settlement: pay from your own rails when `campaign_payout.payable` fires, then call this with your payout id in `externalReference` (required in this mode). - `treasury` settlement: send `recordOnly: true` to record a payout you made yourself (the webhook then carries `recorded: true`). Without it the call answers 409: Zernio pays creators of these campaigns by card with `POST /v1/creator-campaigns/{campaignId}/payout-batches`, never from your balance. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**participant_id** | **String** | Participant ID. | [required] |
**settle_campaign_participant_request** | [**SettleCampaignParticipantRequest**](SettleCampaignParticipantRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  |  |

### Return type

[**models::SettleCampaignParticipant201Response**](settleCampaignParticipant_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## ship_campaign_sample

> models::ApproveCampaignSample200Response ship_campaign_sample(campaign_id, sample_id, idempotency_key, ship_campaign_sample_request)
Mark campaign sample shipped

Records that you sent an `approved` sample yourself, with an optional tracking link, emails the creator and fires `campaign_sample.shipped`. No store call or money is involved. Any other status answers 409. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Campaign ID. | [required] |
**sample_id** | **String** | Sample request ID. | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  |  |
**ship_campaign_sample_request** | Option<[**ShipCampaignSampleRequest**](ShipCampaignSampleRequest.md)> | Optional: no body marks the sample shipped without a tracking link. |  |

### Return type

[**models::ApproveCampaignSample200Response**](approveCampaignSample_200_response.md)

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

