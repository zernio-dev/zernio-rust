# \TreasuryApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cancel_payout_batch**](TreasuryApi.md#cancel_payout_batch) | **POST** /v1/payout-batches/{batchId}/cancel | Cancel an unpaid payout batch
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

Ends the Stripe Checkout of a batch that is still `awaiting_payment` and makes every amount payable again right away, instead of after Stripe's 24-hour expiry. A batch that was already paid is returned unchanged. Needs an owner, admin or billing admin, signed in or through a full-access key they created. 

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

Starts a Stripe Checkout session to fund your balance by card. Card top-ups pay Stripe's processing fee and become available after 7 days. Bank transfers are not available yet; `method: bank_transfer` returns 400. Needs an owner, admin or billing admin, signed in or through a full-access key they created.

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

Moves money from your balance to a payee.  ### Fee  The payee receives the full `amountCents`. Zernio's fee (4%, 50 cent minimum) is added on top, so your balance is debited `totalCents` = `amountCents` + `feeCents`.  ### Who can call it  Needs an owner, admin or billing admin, signed in or through a full-access key they created. A profile-scoped key answers 403.  ### Errors  - 402: the balance does not cover the amount plus the fee. - 402: the balance is negative after a dispute or refund of a card top-up (\"Your balance is negative after a dispute or refund of a card top-up. Add funds to cover it before sending transfers.\"). - 409: the payee has not finished onboarding, or the Idempotency-Key is still processing.  ### Retries  A same-key retry never makes the transfer twice within Stripe's 24-hour idempotency window. It answers 409 while another request is still waiting on Stripe for it.  A transfer Stripe has not confirmed after 24 hours answers 409 until the daily reconciliation marks it paid (Stripe made it) or failed (it did not). 

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

Returns your team's balance:  - the balance you can transfer - card top-ups still on hold - top-ups still waiting for payment - your latest top-ups  Card top-ups become available after 7 days.  A transfer debits its amount plus the fee added on top; the payee receives the full amount.  A card dispute or refund on a top-up is debited from the available balance and can make it negative. Transfers are refused until it is positive again.  A profile-scoped key answers 403, since the balance belongs to the whole team. 

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

