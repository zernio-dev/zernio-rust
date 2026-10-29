# \TreasuryApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cancel_payout_batch**](TreasuryApi.md#cancel_payout_batch) | **POST** /v1/payout-batches/{batchId}/cancel | Cancel an unpaid payout batch
[**cancel_topup**](TreasuryApi.md#cancel_topup) | **POST** /v1/balance/top-ups/{topupId}/cancel | Cancel a top-up
[**confirm_payout_batch**](TreasuryApi.md#confirm_payout_batch) | **POST** /v1/payout-batches/{batchId}/confirm | Confirm a payout batch payment
[**confirm_topup**](TreasuryApi.md#confirm_topup) | **POST** /v1/balance/top-ups/{topupId}/confirm | Confirm a top-up
[**create_payee_onboarding_link**](TreasuryApi.md#create_payee_onboarding_link) | **POST** /v1/payees/{payeeId}/onboarding-link | Create a payee onboarding link
[**create_topup**](TreasuryApi.md#create_topup) | **POST** /v1/balance/top-ups | Create a top-up
[**create_transfer**](TreasuryApi.md#create_transfer) | **POST** /v1/transfers | Create a transfer
[**get_balance**](TreasuryApi.md#get_balance) | **GET** /v1/balance | Get balance
[**get_payout_batch**](TreasuryApi.md#get_payout_batch) | **GET** /v1/payout-batches/{batchId} | Get a payout batch
[**get_topup_receipt**](TreasuryApi.md#get_topup_receipt) | **GET** /v1/balance/top-ups/{topupId}/receipt | Get a top-up receipt
[**get_transfer**](TreasuryApi.md#get_transfer) | **GET** /v1/transfers/{transferId} | Get a transfer
[**list_payees**](TreasuryApi.md#list_payees) | **GET** /v1/payees | List payees
[**list_topups**](TreasuryApi.md#list_topups) | **GET** /v1/balance/top-ups | List top-ups
[**list_transfers**](TreasuryApi.md#list_transfers) | **GET** /v1/transfers | List transfers



## cancel_payout_batch

> models::GetPayoutBatch200Response cancel_payout_batch(batch_id)
Cancel an unpaid payout batch

Ends the payment of a batch that is still `awaiting_payment` (3D Secure left unfinished) and makes every amount payable again right away.  - When Stripe reports the charge already made, the batch is paid out instead. - A batch that was already paid is returned unchanged.  Needs an owner, admin or billing admin, signed in or through a full-access key they created. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**batch_id** | **String** | Payout batch ID. | [required] |

### Return type

[**models::GetPayoutBatch200Response**](getPayoutBatch_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## cancel_topup

> models::TreasuryTopup cancel_topup(topup_id)
Cancel a top-up

Ends the payment of a pending top-up (3D Secure left unfinished), so it stops counting toward `pendingTopupCents`, and returns it as `expired`.  - When Stripe reports it already paid, the top-up is credited and comes back `succeeded`. - A top-up that is no longer pending comes back unchanged. - A creator payout payment (`purpose: payout_batch`) answers 409; cancel it from its campaign.  Needs an owner, admin or billing admin, signed in or through a full-access key they created. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**topup_id** | **String** |  | [required] |

### Return type

[**models::TreasuryTopup**](TreasuryTopup.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## confirm_payout_batch

> models::GetPayoutBatch200Response confirm_payout_batch(batch_id)
Confirm a payout batch payment

Call after 3D Secure. Reads the batch's payment from Stripe, then:  - charge succeeded: pays the creators (`paying`, then `paid`). - bank refused: ends the batch (`failed`) and makes every amount payable again. - still settling: leaves it `awaiting_payment`.  Safe to repeat. Needs an owner, admin or billing admin, signed in or through a full-access key they created. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**batch_id** | **String** | Payout batch ID. | [required] |

### Return type

[**models::GetPayoutBatch200Response**](getPayoutBatch_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## confirm_topup

> models::TreasuryTopup confirm_topup(topup_id)
Confirm a top-up

Call after 3D Secure. Reads the payment from Stripe, then:  - `succeeded`: paid, the top-up is credited. - `failed`: the bank refused it. - `pending`: Stripe is still settling the charge.  Safe to repeat. Needs an owner, admin or billing admin, signed in or through a full-access key they created. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**topup_id** | **String** |  | [required] |

### Return type

[**models::TreasuryTopup**](TreasuryTopup.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_payee_onboarding_link

> models::CreatePayeeOnboardingLink200Response create_payee_onboarding_link(payee_id)
Create a payee onboarding link

Returns a Stripe-hosted link where the payee completes identity and bank details so they can receive payouts.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**payee_id** | **String** |  | [required] |

### Return type

[**models::CreatePayeeOnboardingLink200Response**](createPayeeOnboardingLink_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_topup

> models::CreateTopup201Response create_topup(create_topup_request, idempotency_key)
Create a top-up

Charges the billing owner's saved card (the default one, or `paymentMethodId`) for `amountCents` while the payer is present.  - `status: succeeded`: the card was charged. The top-up is credited to `availableCents` within seconds, net of Stripe's processing fee. Transfers to payees can use it from 7 days after the charge. - `status: requires_action`: the bank asked for 3D Secure. Complete it with Stripe.js `handleNextAction({ clientSecret })`, then call `POST /v1/balance/top-ups/{topupId}/confirm`. One left unconfirmed is cancelled after 30 minutes.  ### Errors  - 402 `payment_required`: no saved card. - 402 `card_declined`: the bank's reason. - 400: `method: bank_transfer` (bank transfers are not available yet).  Needs an owner, admin or billing admin, signed in or through a full-access key they created. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_topup_request** | [**CreateTopupRequest**](CreateTopupRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  |  |

### Return type

[**models::CreateTopup201Response**](createTopup_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_transfer

> models::TreasuryTransfer create_transfer(create_transfer_request, idempotency_key)
Create a transfer

Moves money from your balance to a payee.  ### Fee  The payee receives the full `amountCents`. Zernio's fee (4%, 50 cent minimum) is added on top, so your balance is debited `totalCents` = `amountCents` + `feeCents`.  ### Who can call it  Needs an owner, admin or billing admin, signed in or through a full-access key they created. A profile-scoped key answers 403.  ### Errors  - 402: the balance does not cover the amount plus the fee. - 402: the balance is negative after a dispute or refund of a card top-up (\"Your balance is negative after a dispute or refund of a card top-up. Add funds to cover it before sending transfers.\"). - 409: the payee has not finished onboarding, or the Idempotency-Key is still processing. - 409 `payout_funds_locked`: money from a card top-up can be transferred from 7 days after the charge. The message names the amount and the day (\"$100.00 from your card top-up on Oct 29 can be paid out from Nov 5.\").  ### Retries  A same-key retry never makes the transfer twice within Stripe's 24-hour idempotency window. It answers 409 while another request is still waiting on Stripe for it.  A transfer Stripe has not confirmed after 24 hours answers 409 until the daily reconciliation marks it paid (Stripe made it) or failed (it did not). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_transfer_request** | [**CreateTransferRequest**](CreateTransferRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  |  |

### Return type

[**models::TreasuryTransfer**](TreasuryTransfer.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_balance

> models::GetBalance200Response get_balance()
Get balance

Returns your team's balance:  - the balance you can transfer - the part of it that cannot be paid out to creators yet (`payoutLockedCents`, `payoutLocks`) - top-ups still waiting for payment - your latest top-ups  A card top-up is in `availableCents` as soon as it is paid. Transfers to payees can use it from 7 days after the charge, so a stolen card cannot be turned straight into payouts.  A transfer debits its amount plus the fee added on top; the payee receives the full amount.  A card dispute or refund on a top-up is debited from the available balance and can make it negative. Transfers are refused until it is positive again.  A profile-scoped key answers 403, since the balance belongs to the whole team. 

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::GetBalance200Response**](getBalance_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_payout_batch

> models::GetPayoutBatch200Response get_payout_batch(batch_id)
Get a payout batch

One payout batch with its status and each creator's item. Poll it after the card payment to see when every creator is paid.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**batch_id** | **String** | Payout batch ID. | [required] |

### Return type

[**models::GetPayoutBatch200Response**](getPayoutBatch_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_topup_receipt

> models::GetTopupReceipt200Response get_topup_receipt(topup_id)
Get a top-up receipt

The receipt for a paid top-up or creator payout payment (`purpose: payout_batch`). `format: pdf` is the Stripe invoice PDF; `format: page` is Stripe's receipt page, for payments that have no invoice. The link is short-lived, so fetch it when you need it. A profile-scoped key answers 403.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**topup_id** | **String** |  | [required] |

### Return type

[**models::GetTopupReceipt200Response**](getTopupReceipt_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_transfer

> models::TreasuryTransfer get_transfer(transfer_id)
Get a transfer

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**transfer_id** | **String** |  | [required] |

### Return type

[**models::TreasuryTransfer**](TreasuryTransfer.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_payees

> models::ListPayees200Response list_payees()
List payees

Payees you can transfer to. A payee can receive transfers once `payoutsEnabled` is true. A profile-scoped key answers 403.

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::ListPayees200Response**](listPayees_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_topups

> models::ListTopups200Response list_topups(limit, skip)
List top-ups

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**limit** | Option<**i32**> |  |  |[default to 50]
**skip** | Option<**i32**> |  |  |[default to 0]

### Return type

[**models::ListTopups200Response**](listTopups_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_transfers

> models::ListTransfers200Response list_transfers(limit, skip)
List transfers

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**limit** | Option<**i32**> |  |  |[default to 50]
**skip** | Option<**i32**> |  |  |[default to 0]

### Return type

[**models::ListTransfers200Response**](listTransfers_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

