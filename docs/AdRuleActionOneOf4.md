# AdRuleActionOneOf4

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **Type** | Move the bid cap or cost cap of a Meta ad set, in the ad account currency. Ad set rules on Meta only. An ad set without a cap is skipped with `no_bid_cap`. (enum: adjust_bid) | 
**amount** | Option<**f64**> | The cap to set. | [optional]
**direction** | Option<**Direction**> |  (enum: increase, decrease) | [optional]
**percent** | Option<**i32**> | Step size. A decrease is at most 90. | [optional]
**limit** | Option<**f64**> | The cap never goes above this on an increase, or below it on a decrease. | [optional]
**max_changes_per_day** | Option<**i32**> | At most this many objects changed in any 24 hours, across runs. Matches over the limit are skipped with `daily_limit_reached` and tried again later. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


