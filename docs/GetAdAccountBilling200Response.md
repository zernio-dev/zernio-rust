# GetAdAccountBilling200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**customer_id** | Option<**String**> |  | [optional]
**payments_accounts** | Option<[**Vec<models::GetAdAccountBilling200ResponsePaymentsAccountsInner>**](GetAdAccountBilling200ResponsePaymentsAccountsInner.md)> |  | [optional]
**billing_setups** | Option<[**Vec<models::GetAdAccountBilling200ResponseBillingSetupsInner>**](GetAdAccountBilling200ResponseBillingSetupsInner.md)> |  | [optional]
**account_budgets** | Option<[**Vec<models::GetAdAccountBilling200ResponseAccountBudgetsInner>**](GetAdAccountBilling200ResponseAccountBudgetsInner.md)> |  | [optional]
**pending_budget_proposals** | Option<[**Vec<models::GetAdAccountBilling200ResponsePendingBudgetProposalsInner>**](GetAdAccountBilling200ResponsePendingBudgetProposalsInner.md)> | New account budgets proposed but not yet approved by Google. A setup with one is not reused by the POST. | [optional]
**cached_at** | Option<**String**> | When this data was fetched from Google. Null when the cache is unavailable. | [optional]
**stale** | Option<**bool**> | True when Google's quota was exhausted and this is the last successful fetch. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


