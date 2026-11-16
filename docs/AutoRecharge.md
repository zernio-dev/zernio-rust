# AutoRecharge

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** | Whether auto top-up is on. Charges happen only when this is true and disabledReason is null. | 
**below_cents** | **i32** | The below amount, in cents: when the balance drops below this, auto top-up brings it back to toCents. | 
**to_cents** | **i32** | The back-to amount, in cents. The charge is toCents minus the balance, plus tax. | 
**monthly_limit_cents** | Option<**i32**> | Most auto top-up may add per calendar month (UTC), before tax; null for no limit. | 
**alert_below_cents** | Option<**i32**> | Low-balance email threshold, sent once per drop below it; null for none. | 
**disabled_reason** | Option<**DisabledReason**> | `payment_failed` after four failed charges in a row. Updating the card clears it. (enum: payment_failed, ) | 
**retry_count** | **i32** | Failed charges in a row; 0 once one goes through. | 
**next_retry_at** | Option<**String**> | When a declined auto top-up is tried again; null when none is waiting. | 
**month_recharged_cents** | **i32** | Auto top-ups this calendar month (UTC), paid or being paid, before tax. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


