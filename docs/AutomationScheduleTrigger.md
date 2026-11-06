# AutomationScheduleTrigger

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **Type** |  (enum: schedule) | 
**every** | Option<**Every**> | Run every interval. Send this or `times`, not both. (enum: 15m, 30m, 1h, 3h, 6h, 12h, 1d) | [optional]
**times** | Option<[**Vec<models::AutomationScheduleTriggerTimesInner>**](AutomationScheduleTriggerTimesInner.md)> | Set weekly times. Send this or `every`, not both. | [optional]
**starts_at** | Option<**String**> | Runs from this time on. | [optional]
**ends_at** | Option<**String**> | Stops running after this time. Must be after `startsAt`. | [optional]
**quiet_hours** | Option<[**models::AutomationScheduleTriggerQuietHours**](AutomationScheduleTriggerQuietHours.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


