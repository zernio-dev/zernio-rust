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
**approval_status** | Option<**String**> | X and Reddit only. X's own ad account approval status, or Reddit's `admin_approval`. Observed X values are `ACCEPTED`, `PENDING` and `REJECTED`, but X does not publish the full vocabulary, so treat an unrecognised value as not usable. Other platforms report `accountStatus` or `status` instead. | [optional]
**timezone** | Option<**String**> | Reddit only. The ad account's time zone as Reddit reports it (`time_zone_id`). Schedules on Reddit ads are read in this zone. | [optional]
**r#type** | Option<**String**> | Reddit only. Reddit's ad account type, forwarded unchanged. | [optional]
**disable_reason** | Option<**i32**> | Meta only. Meta's `disable_reason` code, forwarded unchanged.  Present when `accountStatus` is `2` (DISABLED) and Meta gives a reason; this separates a policy action from a payment problem. Absent when Meta reports no reason, or the connected token cannot read the field.  Meta publishes no stable list of values, so none are enumerated here: resolve the code against Meta's own ad account reference. | [optional]
**balance** | Option<**f64**> | TikTok only. Total balance the advertiser can spend (cash plus grant), in whole units of `currency`.  Read from the Business Center balance when the connection has a finance role there: the only TikTok source that counts cash held in a shared payment portfolio. Otherwise TikTok's advertiser-level balance, which can read 0 for a cash-funded advertiser. | [optional]
**cash_balance** | Option<**f64**> | TikTok only. Cash part of `balance`, in whole units of `currency`. Absent when the connection has no finance role in the advertiser's Business Center. | [optional]
**grant_balance** | Option<**f64**> | TikTok only. Grant (ad credit) part of `balance`, in whole units of `currency`. Absent when the connection has no finance role in the advertiser's Business Center. | [optional]
**timezone_name** | Option<**String**> | IANA timezone of the ad account (Meta only). Drives daily-budget reset and Insights day boundaries. | [optional]
**timezone_offset_hours_utc** | Option<**f64**> | Signed UTC offset in hours, reflecting current DST (Meta only). | [optional]
**minimum_daily_budget** | Option<**f64**> | Meta only. Minimum daily budget for the account, in the account currency's major units. This is the impressions-billed minimum; other billing events have higher minimums. Absent when the connected token cannot read it. | [optional]
**funding_source** | Option<**String**> | Meta only. Meta's `funding_source` ID for the ad account, forwarded unchanged. ABSENT both when this connection's token cannot see billing and when the account has no payment method; read `billingStatus` to tell the two apart. | [optional]
**funding_source_details** | Option<[**models::ListAdAccounts200ResponseAccountsInnerFundingSourceDetails**](ListAdAccounts200ResponseAccountsInnerFundingSourceDetails.md)> |  | [optional]
**billing_status** | Option<**BillingStatus**> | Meta only. Whether the ad account has a payment method:  - `missing`: `accountStatus` is `3` (UNSETTLED) or `9` (IN_GRACE_PERIOD), `disableReason` is `3` (RISK_PAYMENT), or the connected person has the MANAGE task on the account (admin, who always sees billing) and Meta returns no funding source. - `missing`, effect: ad creation fails at the ad step with Meta code 100 / subcode 1359188. Add a payment method in Meta's Billing & payments center. - `ok`: Meta returns a funding source. This is presence, not validity: Meta can still refuse the card or balance at ad creation. - `unknown`: the connected person is not an admin of the account, or the token cannot read the billing fields.  (enum: ok, missing, unknown) | [optional]
**selectable** | Option<**bool**> | Meta and X only. Whether the account can create/run ads now. Always present on every Meta and X account. Absent (treat as true) on other platforms. | [optional]
**unusable_reason** | Option<**String**> | Meta and X only. Always present on every Meta and X account. Human-readable reason when selectable is false; null when selectable. | [optional]
**selected** | Option<**bool**> | Always present. True when the ad account is in this connection's ad-account selection, or when the connection has no selection (then every ad account is usable).  - For a posting account (e.g. facebook, twitter), the selection of its ads connection applies. - Unrelated to `selectable`, which is the platform's own status. - Writes to an ad account with `selected: false` answer 403 `ad_account_not_selected`. - `inScopeOnly=true` lists only the selected ones. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


