# \LedgerApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_ledger_balances**](LedgerApi.md#get_ledger_balances) | **GET** /v1/ledger/balances | Get ledger balances
[**list_ledger_entries**](LedgerApi.md#list_ledger_entries) | **GET** /v1/ledger/entries | List ledger entries



## get_ledger_balances

> models::GetLedgerBalances200Response get_ledger_balances(scope_type, scope_id, currency)
Get ledger balances

Returns the balance of each bucket (for example accruing, owed, payable) for one ledger scope.  These return an empty balances object:  - A scope owned by another team. - For a profile-scoped key (or a member limited to some profiles), any scope other than `campaign` and `participant` scopes of campaigns under its profiles. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**scope_type** | **String** | Scope type, for example participant or campaign. | [required] |
**scope_id** | **String** | Scope identifier. | [required] |
**currency** | Option<**String**> | Lowercase ISO 4217 currency code. |  |[default to usd]

### Return type

[**models::GetLedgerBalances200Response**](getLedgerBalances_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ledger_entries

> models::ListLedgerEntries200Response list_ledger_entries(scope_type, scope_id, kind, reference_type, reference_id, limit, skip)
List ledger entries

Lists ledger entries for your team, newest first.  ### Filters  - scope (matches either side of the entry) - kind - the reference that caused the entry  ### Profile-scoped access  A profile-scoped key (or a member limited to some profiles) only sees entries of campaigns under its profiles and of their participants. Operator and platform scopes stay hidden from it. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**scope_type** | Option<**String**> |  |  |
**scope_id** | Option<**String**> |  |  |
**kind** | Option<**String**> |  |  |
**reference_type** | Option<**String**> |  |  |
**reference_id** | Option<**String**> |  |  |
**limit** | Option<**i32**> |  |  |[default to 50]
**skip** | Option<**i32**> |  |  |[default to 0]

### Return type

[**models::ListLedgerEntries200Response**](listLedgerEntries_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

