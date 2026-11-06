# AutomationSubjects

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**each** | **Each** | The objects judged one by one. (enum: campaign, adset, ad) | 
**ad_accounts** | [**Vec<models::AutomationSubjectsAdAccountsInner>**](AutomationSubjectsAdAccountsInner.md) | The ad account to check. One per ad rule, and an edit cannot move it to another. | 
**campaign_ids** | Option<**Vec<String>**> | Only these platform campaigns or their ad sets and ads. Leave out to check the whole ad account. | [optional]
**filters** | Option<[**Vec<models::AutomationAdFilter>**](AutomationAdFilter.md)> | All must hold. | [optional]
**groups** | Option<[**Vec<models::AutomationSubjectsGroupsInner>**](AutomationSubjectsGroupsInner.md)> | Judges campaigns together (campaign rules only): each group's numbers are summed and its rates computed on the totals, and a matching group acts on each of its campaigns.  A group with no filters holds every campaign the rule checks. `reach` and `frequency` cannot be used with groups.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


