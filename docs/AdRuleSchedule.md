# AdRuleSchedule

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**every_minutes** | Option<**EveryMinutes**> | How often the rule runs, in minutes. Null on a rule that runs at set times. (enum: 15, 30, 60, 180, 360, 720, 1440, ) | [optional]
**times** | Option<[**Vec<models::AdRuleScheduleTimesInner>**](AdRuleScheduleTimesInner.md)> | Set weekly times in the ad account timezone, instead of an interval. A rule that changes ads needs a cooldown of at least the shortest gap between two times. | [optional]
**starts_at** | Option<**String**> | The rule runs from this time on. | [optional]
**ends_at** | Option<**String**> | The rule stops running after this time. | [optional]
**quiet_hours** | Option<[**models::AdRuleScheduleQuietHours**](AdRuleScheduleQuietHours.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


