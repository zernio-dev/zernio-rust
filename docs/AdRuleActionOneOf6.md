# AdRuleActionOneOf6

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **Type** | Move daily budget from the matched objects ranked worst by `metric` to those ranked best, keeping the total the same. Not with `lifecycle` or `groups`.  Campaign or ad set rules where the budget sits at that level: objects whose budget sits at another level (Meta CBO and ad set budgets), Google shared budgets and lifetime budgets are left out.  Changes are reserved all at once: when `maxChangesPerDay` would hold back any of them, none is made. A receiver is raised only after every giver's cut applied (else it fails with `reallocation_incomplete` and the move is tried again next run).  Amounts move in the currency's smallest unit (whole units for JPY or KRW). Counts as raising live spend for the free ads allowance. (enum: reallocate_budget) | 
**metric** | **String** | What objects are ranked by: any condition metric except `day_of_month` and `working_day_of_month`, or a result metric (`result:<key>`) on campaign rules.  Objects without a value are not ranked, except one that spent with no result on a metric where lower is best (a CPA with no conversions): it ranks worst and only gives. | 
**window** | **String** | The period the metric is read over, like a condition window. | 
**best** | Option<**Best**> | Which end of the ranking is best. Defaults to `lowest` for `cpa`, `cpc`, `cpm`, `frequency` and result metrics whose formula has spend above the line (cost per sale, %CAC), `highest` otherwise. (enum: highest, lowest) | [optional]
**from** | [**models::AdRuleActionOneOf6From**](AdRuleActionOneOf6From.md) |  | 
**to** | [**models::AdRuleActionOneOf6To**](AdRuleActionOneOf6To.md) |  | 
**percent** | Option<**i32**> | The share of each giver's daily budget it gives. | [optional]
**amount** | Option<**f64**> | The total to move each run, in the ad account currency, taken evenly from the givers. | [optional]
**min_budget** | Option<**f64**> | A giver never goes below this daily budget. A giver also always keeps a tenth of its budget. | [optional]
**max_budget** | Option<**f64**> | A receiver never goes above this daily budget; what receivers cannot take stays with the givers. | [optional]
**max_changes_per_day** | Option<**i32**> | At most this many objects changed in any 24 hours, across runs. Matches over the limit are skipped with `daily_limit_reached` and tried again later. | [optional]
**max_changes_per_object** | Option<**i32**> | At most this many changes to one object by this rule, counted over the last 400 days. An object at the limit is left alone like one in cooldown. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


