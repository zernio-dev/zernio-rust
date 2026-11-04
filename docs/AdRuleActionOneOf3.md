# AdRuleActionOneOf3

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **Type** | Copy the campaign or ad set with its ads, on Meta and TikTok campaigns and ad sets and LinkedIn campaigns. Not on ad-level rules. (enum: duplicate) | 
**status** | Option<**Status**> | How the copy starts. Defaults to `paused`. (enum: paused, active) | [optional]
**rename_suffix** | Option<**String**> | Text added to the copy's name. | [optional]
**max_changes_per_day** | Option<**i32**> | At most this many objects changed in any 24 hours, across runs. Matches over the limit are skipped with `daily_limit_reached` and tried again later. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


