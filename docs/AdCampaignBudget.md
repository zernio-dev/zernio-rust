# AdCampaignBudget

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**amount** | **f64** |  | 
**r#type** | **Type** |  (enum: daily, lifetime) | 
**amount_micros** | Option<**String**> | Google only. Exact decimal micros; DAILY uses amount_micros and CUSTOM_PERIOD uses total_amount_micros. | [optional]
**explicitly_shared** | Option<**bool**> | Google only. True for a shared budget; null when unavailable. Shared writes require allowSharedBudgetUpdate=true; unknown sharing status cannot be overridden. | [optional]
**resource_name** | Option<**String**> | Google only. campaign_budget.resource_name, or null when unavailable. | [optional]
**delivery_method** | Option<**String**> | Google only. campaign_budget.delivery_method, typically STANDARD, or null when unavailable. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


