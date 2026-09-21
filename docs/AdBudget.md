# AdBudget

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**amount** | Option<**f64**> |  | [optional]
**r#type** | Option<**Type**> |  (enum: daily, lifetime) | [optional]
**daily** | Option<**f64**> | LinkedIn only. The parent campaign's `dailyBudget`. LinkedIn allows a daily AND a lifetime budget on the same campaign, which `amount`/`type` cannot express (daily wins there); read `daily` and `lifetime` to see both. | [optional]
**lifetime** | Option<**f64**> | LinkedIn only. The parent campaign's `totalBudget`, readable even when a daily budget is also set. | [optional]
**pacing** | Option<**String**> | LinkedIn only. The campaign's `pacingStrategy`: how fast LinkedIn may spend the budget. Typically LINEAR or ACCELERATED; the list is open. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


