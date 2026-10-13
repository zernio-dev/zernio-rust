# AdBudget

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**amount** | Option<**f64**> |  | [optional]
**r#type** | Option<**Type**> |  (enum: daily, lifetime) | [optional]
**daily** | Option<**f64**> | LinkedIn and X only. The daily budget (LinkedIn: the parent campaign's `dailyBudget`; X: the line item's, or the campaign's when the line item has none). Both allow a daily AND a lifetime budget together, which `amount`/`type` cannot express (daily wins there); read `daily` and `lifetime` to see both. | [optional]
**lifetime** | Option<**f64**> | LinkedIn and X only. The lifetime total (LinkedIn: the parent campaign's `totalBudget`; X: `total_budget_amount_local_micro`, for example the `lifetimeBudgetCap` of a boost), readable even when a daily budget is also set. | [optional]
**pacing** | Option<**String**> | LinkedIn only. The campaign's `pacingStrategy`: how fast LinkedIn may spend the budget. Typically LINEAR or ACCELERATED; the list is open. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


