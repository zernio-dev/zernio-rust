# AdRuleLifecycle

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**confirm_checks** | Option<**i32**> | Matching runs in a row before acting. Defaults to 1. | [optional]
**hold** | Option<[**models::AdRuleConditions**](AdRuleConditions.md)> | Keeps an open alert open after the conditions stop matching. | [optional]
**critical** | Option<[**models::AdRuleConditions**](AdRuleConditions.md)> | Marks an open alert critical. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


