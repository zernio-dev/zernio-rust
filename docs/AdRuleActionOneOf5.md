# AdRuleActionOneOf5

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **Type** | Move a Google campaign's target CPA or target ROAS inside the strategy it is on (Target CPA or Maximize conversions for `cpa`, Target ROAS or Maximize conversion value for `roas`), never switching strategies. Campaign rules on Google only.  Skipped with `portfolio_bid_strategy` on a portfolio strategy, `unsupported_bid_strategy` on one with no target (Manual CPC, Maximize clicks), and `no_target_cpa` or `no_target_roas` when the strategy holds no such target. A target CPA in a zero-decimal currency is rounded to whole units. (enum: adjust_target) | 
**target** | **Target** | Which target moves: `cpa` in the ad account currency, `roas` as a ratio (3 is 300%). (enum: cpa, roas) | 
**amount** | Option<**f64**> | The target to set. | [optional]
**direction** | Option<**Direction**> |  (enum: increase, decrease) | [optional]
**percent** | Option<**i32**> | Step size. A decrease is at most 90. | [optional]
**limit** | Option<**f64**> | The target never goes above this on an increase, or below it on a decrease. | [optional]
**max_changes_per_day** | Option<**i32**> | At most this many objects changed in any 24 hours, across runs. Matches over the limit are skipped with `daily_limit_reached` and tried again later. | [optional]
**max_changes_per_object** | Option<**i32**> | At most this many changes to one object by this rule, counted over the last 400 days. An object at the limit is left alone like one in cooldown. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


