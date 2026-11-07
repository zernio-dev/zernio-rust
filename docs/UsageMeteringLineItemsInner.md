# UsageMeteringLineItemsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | Option<**String**> |  | [optional]
**product** | Option<**Product**> |  (enum: accounts, numbers, imessage, calls, sms, messages, verify, dlc, xApi, ads, credits, other) | [optional]
**total_usd** | Option<**f64**> |  | [optional]
**quantity** | Option<**f64**> |  | [optional]
**paid_from** | Option<**PaidFrom**> | Present only on pay-per-use paid from the prepaid balance (balance billing). That spend is included in `days` and `totals` but is not on the monthly invoice. (enum: balance) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


