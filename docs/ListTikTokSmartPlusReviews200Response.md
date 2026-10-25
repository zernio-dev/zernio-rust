# ListTikTokSmartPlusReviews200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ad_account_id** | Option<**String**> |  | [optional]
**include_deleted** | Option<**bool**> |  | [optional]
**max_age_seconds** | Option<**i32**> | The freshness window this page was read with. | [optional]
**page** | Option<**i32**> |  | [optional]
**page_size** | Option<**i32**> |  | [optional]
**total_pages** | Option<**i32**> |  | [optional]
**total_smart_plus_ads** | Option<**i32**> | Smart+ ads of the advertiser across all pages. | [optional]
**listing** | Option<[**models::ListTikTokSmartPlusReviews200ResponseListing**](ListTikTokSmartPlusReviews200ResponseListing.md)> |  | [optional]
**review_error** | Option<[**models::ListTikTokSmartPlusReviews200ResponseReviewError**](ListTikTokSmartPlusReviews200ResponseReviewError.md)> |  | [optional]
**counts** | Option<[**models::ListTikTokSmartPlusReviews200ResponseCounts**](ListTikTokSmartPlusReviews200ResponseCounts.md)> |  | [optional]
**oldest_read_at** | Option<**String**> | The oldest `readAt` in `items`. Null when `items` is empty. | [optional]
**items** | Option<[**Vec<models::ListTikTokSmartPlusReviews200ResponseItemsInner>**](ListTikTokSmartPlusReviews200ResponseItemsInner.md)> |  | [optional]
**failed_smart_plus_ads** | Option<[**Vec<models::ListTikTokSmartPlusReviews200ResponseFailedSmartPlusAdsInner>**](ListTikTokSmartPlusReviews200ResponseFailedSmartPlusAdsInner.md)> | Smart+ ads of this page whose review TikTok refused on its own (for example an ad deleted on TikTok since the listing was read). Zernio splits a refused batch in halves (at most 16 extra calls per page), so the other ads of the batch are still read; ads left unresolved by that cap stay in `items` with their stored review or in `pendingSmartPlusAdIds`. Empty when none. | [optional]
**incomplete** | Option<**bool**> | True while some Smart+ ads of this page were never read (`counts.pending > 0`). Stale items alone keep it false. | [optional]
**all_fresh** | Option<**bool**> | True when every item and refusal of this page was read within `maxAgeSeconds` and nothing is pending. False with `incomplete: false` means the page is complete but some reviews are older than the window; a later read refreshes them oldest first. | [optional]
**pending_smart_plus_ad_ids** | Option<**Vec<String>**> | Smart+ ads of this page never read. Empty when every ad has a stored review or refusal. | [optional]
**retry_after_seconds** | Option<**i32**> | Seconds to wait before reading this page again, set only while `incomplete` is true and review reads are paused. Null when complete (stale items included), or when the page is incomplete without a quota pause (read it again right away). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


