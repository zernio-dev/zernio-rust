# UpdateAccountRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**username** | Option<**String**> |  | [optional]
**display_name** | Option<**String**> |  | [optional]
**x_capabilities** | Option<[**models::UpdateAccountRequestXCapabilities**](UpdateAccountRequestXCapabilities.md)> |  | [optional]
**meta_ads_sync_enabled** | Option<**bool**> | Facebook only (400 `invalid_field_value` on any other platform). Off by default for every Facebook account.  `true` makes this account sync the Meta ads of the ad accounts it reaches, like a `metaads` connection.  - The first sync starts at once (14 days, then 90 days of history in the background) and fires `account.ads.initial_sync_completed` for this `accountId` with `platform: metaads`. - It then refreshes on the Meta Ads schedule. - Each switch from `false` to `true` runs another initial sync and fires the webhook again. Sending `true` while it is on changes nothing. - Needs `ads_management` and `ads_read` on the account (403 `reconnect_required` otherwise, with `details.requiredPermissions`). - Needs ads access (403 `ads_addon_required`) and room in the managed ads allowance (403 `ads_allowance_exceeded`). - While a `metaads` connection has this account as `parentAccountId`, that connection syncs the ads instead.  Synced active ads count on the managed ads meter like ads from a Meta Ads connection.  `false` stops the sync. Ads already synced are kept, never deleted: they stop updating and stop counting on the meter, and a `metaads` connection of yours that reaches the same ad account takes them over. Posting, inbox and comments on the account are not affected.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


