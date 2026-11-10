# CreatorCampaignEconomicsRetainer

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **Type** |  (enum: retainer) | 
**mode** | Option<**Mode**> | `standard` pays `amountCents` per period. `smart` guarantees it: the commission the creator earned in the period is topped up to `amountCents`. Smart needs `commission` and a linked store. (enum: standard, smart) | [optional][default to Standard]
**amount_cents** | **i32** |  | 
**period** | **Period** | Weeks start Monday 00:00 UTC, months on the 1st. A period is paid within a day after it ends. A standard `once` retainer pays as soon as the posts are approved; a smart one when the campaign ends. (enum: week, month, once) | 
**required_approved_posts** | **i32** | Posts approved within the period that it needs. 0 pays without posts. | 
**commission** | Option<[**models::CreatorCampaignCommissionTerms**](CreatorCampaignCommissionTerms.md)> |  | [optional]
**budget_cents** | **i32** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


