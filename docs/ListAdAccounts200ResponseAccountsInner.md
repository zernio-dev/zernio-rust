# ListAdAccounts200ResponseAccountsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Platform ad account ID (e.g. act_123) | [optional]
**name** | Option<**String**> |  | [optional]
**currency** | Option<**String**> |  | [optional]
**business_id** | Option<**String**> | Meta only. Owning Business Manager ID when available on the grant. | [optional]
**business_name** | Option<**String**> | Owning business name when supplied by the platform. | [optional]
**status** | Option<**String**> | LinkedIn only. LinkedIn's own ad account status. In practice always `ACTIVE`, because the LinkedIn query filters to active accounts. Meta, Google, TikTok and Pinterest report `accountStatus` instead; X reports `approvalStatus`. | [optional]
**account_status** | Option<**serde_json::Value**> |  | [optional]
**approval_status** | Option<**String**> | X only. X's own ad account approval status. Observed values are `ACCEPTED`, `PENDING` and `REJECTED`, but X does not publish the full vocabulary, so treat an unrecognised value as not usable. Other platforms report `accountStatus` or `status` instead. | [optional]
**disable_reason** | Option<**i32**> | Meta only. Meta's `disable_reason` code, forwarded unchanged. Present when `accountStatus` is `2` (DISABLED) and Meta gives a reason, which is what separates a policy action from a payment problem. Meta does not publish a stable list of values for this field, so none are enumerated here: resolve the code against Meta's own ad account reference. Absent when Meta reports no reason, or when the connected token cannot read the field. | [optional]
**timezone_name** | Option<**String**> | IANA timezone of the ad account (Meta only). Drives daily-budget reset and Insights day boundaries. | [optional]
**timezone_offset_hours_utc** | Option<**f64**> | Signed UTC offset in hours, reflecting current DST (Meta only). | [optional]
**minimum_daily_budget** | Option<**f64**> | Meta only. Minimum daily budget for the account, in the account currency's major units. This is the impressions-billed minimum; other billing events have higher minimums. Absent when the connected token cannot read it. | [optional]
**funding_source** | Option<**String**> | Meta only. Meta's `funding_source` ID for the ad account, forwarded unchanged. ABSENT both when this connection's token cannot see billing and when the account has no payment method; read `billingStatus` to tell the two apart. | [optional]
**funding_source_details** | Option<[**models::ListAdAccounts200ResponseAccountsInnerFundingSourceDetails**](ListAdAccounts200ResponseAccountsInnerFundingSourceDetails.md)> |  | [optional]
**billing_status** | Option<**BillingStatus**> | Meta only. Whether the ad account has a payment method, derived as follows: - `missing` when `accountStatus` is `3` (UNSETTLED) or `9` (IN_GRACE_PERIOD),   when `disableReason` is `3` (RISK_PAYMENT), or when the connected person   has the MANAGE task on the account (admin, who always sees billing) and   Meta returns no funding source. Ad creation on such an account fails at   the ad step with Meta code 100 / subcode 1359188: add a payment method in   Meta's Billing & payments center. - `ok` when Meta returns a funding source. This is presence, not validity:   Meta can still refuse the card or balance at ad creation. - `unknown` when the connected person is not an admin of the account, or   the token cannot read the billing fields.  (enum: ok, missing, unknown) | [optional]
**selectable** | Option<**bool**> | Meta and X only. Whether the account can create/run ads now. Absent (treat as true) on other platforms. | [optional]
**unusable_reason** | Option<**String**> | Meta and X only. Human-readable reason when selectable is false; null when selectable. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


