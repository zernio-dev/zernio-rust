# GetBalance200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**available_cents** | Option<**i32**> | Balance you can transfer now. Negative after a dispute or refund of a top-up that was already spent; transfers are refused while it is negative. | [optional]
**pending_cents** | Option<**i32**> | Paid card top-ups still on hold. Card top-ups become available after 7 days. | [optional]
**pending_releases** | Option<[**Vec<models::GetBalance200ResponsePendingReleasesInner>**](GetBalance200ResponsePendingReleasesInner.md)> | Card top-ups on hold, each with the time it becomes available. | [optional]
**pending_topup_cents** | Option<**i32**> | Top-ups started but not paid yet. | [optional]
**currency** | Option<**Currency**> |  (enum: usd) | [optional]
**recent_topups** | Option<[**Vec<models::TreasuryTopup>**](TreasuryTopup.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


