# AutomationLimits

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cooldown** | Option<**String**> | How long an object is left alone after the rule acts on it. Whole minutes, up to `30d`. | [optional][default to 1d]
**max_changes_per_day** | Option<**i32**> | Most changes across the last 24 hours. Needs an `ads.*` step. | [optional]
**max_changes_per_object** | Option<**i32**> | Most times the rule may change one object, over its whole history. Needs an `ads.*` step. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


