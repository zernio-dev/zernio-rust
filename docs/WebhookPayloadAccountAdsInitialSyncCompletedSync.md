# WebhookPayloadAccountAdsInitialSyncCompletedSync

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **Status** | Overall outcome of the initial sync. (enum: success, failure) | 
**total_ads** | **i32** | Total number of ads discovered for backfill. | 
**synced** | **i32** | Number of ads successfully synced. | 
**failed** | **i32** | Number of ads that failed to sync. | 
**error** | Option<**String**> | Free-form error message from the platform (typically Meta's Marketing API). Truncated to ~2KB. Present when `status` is `failure` (and sometimes on `success` when discovery saw zero ad accounts). For UX branching prefer `errorCategory`; this field is for human display and debugging.  | [optional]
**error_code** | Option<**String**> | Platform-native error code if parsed (e.g. Meta `190`, `10`, `200`). | [optional]
**error_subcode** | Option<**String**> | Platform-native error subcode if parsed. | [optional]
**error_category** | Option<**ErrorCategory**> | Stable category for UX branching. New values may be added; existing ones are stable. Mapping:   - `token_invalid`: access token is expired or revoked. Reconnect.   - `permission_denied`: token lacks required scope, or the user has no role     on the Business Manager that owns the ad account. Reconnect with full     permissions, or have an admin grant access.   - `no_ad_accounts`: token is valid but sees zero ad accounts. The user     needs to connect a Business Manager that owns ad accounts.   - `rate_limited`: platform throttled us. Sync will retry automatically.   - `discovery_failed`: any other platform-side failure. Inspect `error`.   - `unknown`: classifier could not categorize the failure.  (enum: token_invalid, permission_denied, no_ad_accounts, rate_limited, discovery_failed, unknown) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


