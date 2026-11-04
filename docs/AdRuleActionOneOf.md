# AdRuleActionOneOf

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **Type** | Send the `ad_rule.triggered` webhook, and the alert to every `send` destination. (enum: notify) | 
**send** | Option<[**Vec<models::AdRuleActionOneOfSendInner>**](AdRuleActionOneOfSendInner.md)> | Also send a short alert through accounts you connected: what matched, the values and what the rule did. Up to 5 destinations, checked when the rule is saved.  A destination that fails is reported in the run's `notification`; it never undoes a change.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


