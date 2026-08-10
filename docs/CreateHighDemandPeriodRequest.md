# CreateHighDemandPeriodRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id used to resolve the Meta token. | 
**campaign_id** | Option<**String**> | Platform campaign id. Exactly one of campaignId / adSetId. | [optional]
**ad_set_id** | Option<**String**> | Platform ad set id. Exactly one of campaignId / adSetId. | [optional]
**budget_value** | **f64** | With ABSOLUTE, a budget in the ad account's currency in WHOLE units (50 = $50.00). With MULTIPLIER, a factor of the existing budget (2 = double it) and NOT a currency amount. | 
**budget_value_type** | **BudgetValueType** |  (enum: ABSOLUTE, MULTIPLIER) | 
**time_start** | **i32** | Unix seconds, on a 15-minute boundary (:00, :15, :30, :45). | 
**time_end** | **i32** | Unix seconds, on a 15-minute boundary and after timeStart. | 
**recurrence_type** | Option<**RecurrenceType**> |  (enum: ONE_TIME, WEEKLY, MONTHLY) | [optional]
**currency** | Option<**String**> | Ad account currency, for the ABSOLUTE minor-unit conversion. Ignored for MULTIPLIER. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


