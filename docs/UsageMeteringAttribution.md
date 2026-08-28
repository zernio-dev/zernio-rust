# UsageMeteringAttribution

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**group_by** | Option<**GroupBy**> |  (enum: profile, account) | [optional]
**groups** | Option<[**Vec<models::UsageAttributionGroup>**](UsageAttributionGroup.md)> |  | [optional]
**unattributed** | Option<[**models::UsageAttributionSlice**](UsageAttributionSlice.md)> | Spend no profile/account can claim: credits, 10DLC fees, Verify, and usage whose record no longer resolves to an account. Zero for a restricted principal. | [optional]
**totals** | Option<[**models::UsageAttributionSlice**](UsageAttributionSlice.md)> | The window totals; for a restricted principal, the sum of the visible groups. | [optional]
**restricted** | Option<**bool**> | True when the caller (profile-scoped API key or member) cannot see every profile: `groups` are filtered, `totals` sum them, `unattributed` is zero, and the top-level `days` / `totals` / `lineItems` are projected onto the visible groups with `peaks`, `callUsage` and `tax` null. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


