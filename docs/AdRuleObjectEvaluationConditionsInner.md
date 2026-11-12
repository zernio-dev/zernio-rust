# AdRuleObjectEvaluationConditionsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**metric** | **Metric** |  (enum: spend, impressions, clicks, conversions, ctr, cpc, cpm, cpa, roas, reach, frequency, daily_budget, budget_used, day_of_month, working_day_of_month, search_impression_share, search_budget_lost_impression_share, search_rank_lost_impression_share) | 
**window** | **Window** | Days in the ad account's own timezone. `last_7d` is the 7 full days before today; only `today` and `this_month` read the day in progress.  `this_month` runs from the 1st through today; `last_month` is the whole previous calendar month.  `<from>_to_<to>_days_ago` is any range of full days, both ends included, such as `8_to_2_days_ago` to skip the 2 most recent days while their conversions still arrive. `from` is at least `to` and at most 90.  `last_complete_hour`, `last_3h` and `today_so_far` read campaign totals hour by hour, on campaign rules for Meta and Google, and end at the latest hour whose numbers have settled, not at now. They take `spend`, `impressions`, `clicks`, `ctr`, `cpc` and `cpm`, and no `top` or `bottom`.  (enum: today, yesterday, last_3d, last_7d, last_14d, last_30d, this_month, last_month, last_complete_hour, last_3h, today_so_far) | 
**op** | **Op** | `top` and `bottom` rank the rule's objects by the metric over the window, highest first for `top`, and match the first `value` (a whole number from 1 to 100). Objects with no value are not ranked; the run history shows each one's position. (enum: >, >=, <, <=, top, bottom) | 
**value** | **f64** |  | 
**compare_to** | Option<**String**> | Makes the condition relative: `value` becomes a ratio of the metric over `window` to the same metric over this window, such as `30_to_2_days_ago`.  `previous_period` is the same number of days just before `window`. For `this_month` it is the same days of last month, and for `last_month` the month before.  Spend, impressions, clicks, conversions and reach are compared per day, so windows of different lengths compare fairly; rates such as `cpc` compare as they are. A comparison window with no value never matches.  `usual` compares with the median of the same window on the 4 previous weeks. For an hourly window that is the same hours on the 4 previous same weekdays, and for a window of up to 7 full days (not `today`) the same days moved back 1 to 4 weeks.  `usual` needs at least 3 of those weeks with a value, and takes no reach, frequency, budget or calendar metric.  On an hourly window, `compareTo` is `usual`, or for `ctr`, `cpc` and `cpm` a window of full days ending by yesterday and starting at most 35 days ago, read from the same hourly totals.  For example, `cpc` over `last_complete_hour` `>=` 5 against `last_30d` means the last hour's clicks cost 5 times their 30-day price.  | [optional]
**of** | Option<**Of**> | Reads the usual value of the metric over `window` (as `compareTo: usual` defines it) instead of its current value, such as campaigns that usually get at least 50 impressions in the last 3 hours. Not combined with `compareTo`. (enum: usual) | [optional]
**actual** | Option<**f64**> | The object's value over the window. Null when it cannot be computed. | 
**met** | **bool** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


