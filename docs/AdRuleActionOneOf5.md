# AdRuleActionOneOf5

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **Type** | Tag the object by its name. Meta, Google and LinkedIn campaigns and ad sets, and TikTok campaigns, ad groups and ads. An object whose name already has the tag (or lacks it, for `remove`) is skipped with `name_unchanged`. (enum: edit_name) | 
**add** | Option<**String**> | Text to add, like `[WINNER]`. Compared without case. | [optional]
**at** | Option<**At**> | Where `add` goes. Defaults to `start`. (enum: start, end) | [optional]
**remove** | Option<**String**> | Text to take out of the name, every copy of it. | [optional]
**max_changes_per_day** | Option<**i32**> | At most this many objects changed in any 24 hours, across runs. Matches over the limit are skipped with `daily_limit_reached` and tried again later. | [optional]
**max_changes_per_object** | Option<**i32**> | At most this many changes to one object by this rule, counted over the last 400 days. An object at the limit is left alone like one in cooldown. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


