# ListAdAccounts200ResponseAccountsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Platform ad account ID (e.g. act_123) | [optional]
**name** | Option<**String**> |  | [optional]
**currency** | Option<**String**> |  | [optional]
**status** | Option<**String**> |  | [optional]
**timezone_name** | Option<**String**> | IANA timezone of the ad account (Meta only). Drives daily-budget reset and Insights day boundaries. | [optional]
**timezone_offset_hours_utc** | Option<**f64**> | Signed UTC offset in hours, reflecting current DST (Meta only). | [optional]
**minimum_daily_budget** | Option<**f64**> | Meta only. Minimum daily budget for the account, in the account currency's major units. This is the impressions-billed minimum; other billing events have higher minimums. Absent when the connected token cannot read it. | [optional]
**selectable** | Option<**bool**> | Meta only. Whether the account can create/run ads now. Absent (treat as true) on non-Meta platforms. | [optional]
**unusable_reason** | Option<**String**> | Meta only. Human-readable reason when selectable is false; null when selectable. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


