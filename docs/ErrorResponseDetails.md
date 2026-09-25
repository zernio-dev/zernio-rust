# ErrorResponseDetails

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**stage** | Option<**Stage**> | Meta ad create failures only. The step that failed: `media` (image/video download or upload), `campaign`, `adset`, `creative`, `ad` (the ad POST itself, where Meta's code 31 / 3858385 hold and 100 / 1359188 payment rejections land), `activation` (switching the created objects on), or `other` (a read or check before any write). (enum: media, campaign, adset, creative, ad, activation, other) | [optional]
**ad_account_id** | Option<**String**> | Meta ad create failures only. The ad account the request wrote to (`act_...`). | [optional]
**created_objects** | Option<[**Vec<models::ErrorResponseDetailsCreatedObjectsInner>**](ErrorResponseDetailsCreatedObjectsInner.md)> | Meta ad create failures only. Every object this request created before failing, in creation order. Objects you referenced (an existing campaign, ad set, creative or video) are never listed and never deleted. | [optional]
**unconfirmed_write** | Option<[**models::ErrorResponseDetailsUnconfirmedWrite**](ErrorResponseDetailsUnconfirmedWrite.md)> |  | [optional]
**quota_exhausted** | Option<**bool**> | Google Ads 429 only. True when the upstream Google Ads quota is spent rather than a Zernio limit. | [optional]
**quota_scope** | Option<**QuotaScope**> | Google Ads 429 only, when Google names the scope. DEVELOPER is the shared developer-token budget; ACCOUNT is your ad account. (enum: DEVELOPER, ACCOUNT) | [optional]
**budget_scope** | Option<**BudgetScope**> | Zernio Google Ads operations-budget 429 only (never set alongside `quotaExhausted`). `user` is your own burst/daily allowance; `platform` is the fleet-wide daily budget shared across customers. (enum: user, platform) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


