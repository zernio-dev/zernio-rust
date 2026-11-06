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
[**get_auto_recharge**](TreasuryApi.md#get_auto_recharge) | **GET** /v1/balance/auto-recharge | Get auto-recharge settings
[**get_balance**](TreasuryApi.md#get_balance) | **GET** /v1/balance | Get balance
[**get_payout_batch**](TreasuryApi.md#get_payout_batch) | **GET** /v1/payout-batches/{batchId} | Get a payout batch
[**get_topup_invoice**](TreasuryApi.md#get_topup_invoice) | **GET** /v1/balance/top-ups/{topupId}/invoice | Get a top-up invoice
[**get_topup_receipt**](TreasuryApi.md#get_topup_receipt) | **GET** /v1/balance/top-ups/{topupId}/receipt | Get a top-up receipt
[**get_topup_statement**](TreasuryApi.md#get_topup_statement) | **GET** /v1/balance/top-ups/{topupId}/statement | Get a top-up invoice (alias)
[**get_transfer**](TreasuryApi.md#get_transfer) | **GET** /v1/transfers/{transferId} | Get a transfer
[**list_payees**](TreasuryApi.md#list_payees) | **GET** /v1/payees | List payees
[**list_topups**](TreasuryApi.md#list_topups) | **GET** /v1/balance/top-ups | List top-ups
[**list_transfers**](TreasuryApi.md#list_transfers) | **GET** /v1/transfers | List transfers
[**preview_topup**](TreasuryApi.md#preview_topup) | **POST** /v1/balance/top-ups/preview | Preview a top-up's tax
[**update_auto_recharge**](TreasuryApi.md#update_auto_recharge) | **PATCH** /v1/balance/auto-recharge | Update auto-recharge settings



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

Charges the billing owner's saved card (the default one, or `paymentMethodId`) `amountCents` plus tax, while the payer is present, and credits your balance `amountCents`. There is no card fee.  Tax is added on top of the amount (`taxCents`, `totalCents`): VAT at 21% in Spain, at the customer's country rate for EU consumers; an EU business with a valid VAT id is reverse charged (no VAT, `reverseCharge: true`); outside the EU there is none.  Usage paid from the balance carries no further VAT. Get the figures before paying with `POST /v1/balance/top-ups/preview`.  Each top-up has an invoice, with VAT where it applies (`GET /v1/balance/top-ups/{topupId}/invoice`), and a card receipt (`GET /v1/balance/top-ups/{topupId}/receipt`).  - `status: succeeded`: the card was charged. `amountCents` is credited to `availableCents` within seconds. Transfers to payees can use it from 7 days after the charge. - `status: requires_action`: the bank asked for 3D Secure. Complete it with Stripe.js `handleNextAction({ clientSecret })`, then call `POST /v1/balance/top-ups/{topupId}/confirm`. One left unconfirmed is cancelled after 30 minutes.  ### Errors  - 402 `payment_required`: no saved card. - 402 `card_declined`: the bank's reason. - 400: `method: bank_transfer` (bank transfers are not available yet). - 400 `invalid_billing_address`: the billing address gives no tax location. Add it in Billing, then retry.  Needs an owner, admin or billing admin, signed in or through a full-access key they created. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_topup_request** | [**CreateTopupRequest**](CreateTopupRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  |  |

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
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  |  |

### Return type

[**models::TreasuryTransfer**](TreasuryTransfer.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_auto_recharge

> models::AutoRecharge get_auto_recharge()
Get auto-recharge settings

Your balance's auto-recharge rule: when the balance drops below `belowCents`, the billing owner's saved card is charged back up to `toCents`, tax added on top as for any top-up.  The first read gives the default rule, sized from your last 30 days of pay-per-use: below about a week of spend (at least $5), back up by about two more weeks (at least $20).  - 409 `balance_billing_required`: the account is not on the prepaid balance.  A profile-scoped key answers 403. 

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::AutoRecharge**](AutoRecharge.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
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


## get_topup_invoice

> models::GetTopupInvoice200Response get_topup_invoice(topup_id)
Get a top-up invoice

The invoice for a paid balance top-up: the PDF of the Stripe invoice it was paid through.  It shows the amount added to your balance and the tax charged on top: VAT where it applies, or a reverse charge note for an EU business with a valid VAT id. Usage paid from the balance carries no further VAT.  - `format: pdf` is the invoice PDF; `format: page` is its Stripe-hosted page when the PDF is not ready. - 404 before the top-up is paid, and for a payment with no invoice (top-ups before 2026-11-05, creator payout payments). Its card receipt is at getTopupReceipt.  The link is short-lived, so fetch it when you need it. A profile-scoped key answers 403. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**topup_id** | **String** |  | [required] |

### Return type

[**models::GetTopupInvoice200Response**](getTopupInvoice_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_topup_receipt

> models::GetTopupReceipt200Response get_topup_receipt(topup_id)
Get a top-up receipt

The receipt for a paid top-up or creator payout payment (`purpose: payout_batch`). `url` is the payment's invoice PDF when it has one (`format: pdf`), else Stripe's card receipt page (`format: page`); `invoiceUrl` and `receiptUrl` give each on its own.  The invoice alone is at getTopupInvoice. The link is short-lived, so fetch it when you need it. A profile-scoped key answers 403.

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


## get_topup_statement

> models::GetTopupInvoice200Response get_topup_statement(topup_id)
Get a top-up invoice (alias)

Alias of getTopupInvoice, kept for clients written against its first name.  The invoice for a paid balance top-up: the PDF of the Stripe invoice it was paid through.  It shows the amount added to your balance and the tax charged on top: VAT where it applies, or a reverse charge note for an EU business with a valid VAT id. Usage paid from the balance carries no further VAT.  - `format: pdf` is the invoice PDF; `format: page` is its Stripe-hosted page when the PDF is not ready. - 404 before the top-up is paid, and for a payment with no invoice (top-ups before 2026-11-05, creator payout payments). Its card receipt is at getTopupReceipt.  The link is short-lived, so fetch it when you need it. A profile-scoped key answers 403. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**topup_id** | **String** |  | [required] |

### Return type

[**models::GetTopupInvoice200Response**](getTopupInvoice_200_response.md)

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


## preview_topup

> models::PreviewTopup200Response preview_topup(preview_topup_request)
Preview a top-up's tax

The tax a top-up of `amountCents` will carry and the total the card is charged, calculated by Stripe Tax from the billing owner's billing address and tax ids, as the top-up's invoice will be. Charges nothing.  - 400 `invalid_billing_address`: the billing address gives no tax location, so a top-up would be refused too.  Needs a full-access key or a signed-in session; a profile-scoped key answers 403. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**preview_topup_request** | [**PreviewTopupRequest**](PreviewTopupRequest.md) |  | [required] |

### Return type

[**models::PreviewTopup200Response**](previewTopup_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_auto_recharge

> models::AutoRecharge update_auto_recharge(update_auto_recharge_request)
Update auto-recharge settings

Changes the auto-recharge rule. Omitted fields keep their value.  A declined recharge is retried 1 hour, 1 day and 3 days later, with an email each time. After the last retry fails, auto-recharge switches off (`disabledReason: payment_failed`) until the card is updated. A top-up you make yourself resets the retries.  A bank asking for 3D Secure counts as a decline: the charge happens while you are away, so the email asks you to top up in Billing.  When this month's auto-recharges plus the next one would pass `monthlyLimitCents`, the card is not charged and you get one email that month. At $0, pay-per-use then answers 402 `usage_limit_reached`.  - 400: a field is out of range, or `toCents` is not more than $5 above `belowCents`. - 409 `balance_billing_required`: the account is not on the prepaid balance.  Needs an owner, admin or billing admin, signed in or through a full-access key they created. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**update_auto_recharge_request** | [**UpdateAutoRechargeRequest**](UpdateAutoRechargeRequest.md) |  | [required] |

### Return type

[**models::AutoRecharge**](AutoRecharge.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

