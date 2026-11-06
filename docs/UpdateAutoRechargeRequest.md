# UpdateAutoRechargeRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | Option<**bool**> | Turns auto-recharge on or off. A rule switched off by failed charges stays off until the card is updated. | [optional]
**below_cents** | Option<**i32**> | Recharge when the balance drops below this, in cents. At least $5. | [optional]
**to_cents** | Option<**i32**> | Recharge back up to this, in cents. More than $5 above belowCents. | [optional]
**monthly_limit_cents** | Option<**i32**> | Most auto-recharge may add per calendar month (UTC), before tax. Null for no limit. | [optional]
**alert_below_cents** | Option<**i32**> | Email the billing owner once each time the balance drops below this. Null for no email. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


