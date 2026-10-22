# ListTikTokSmartPlusReviews200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ad_account_id** | Option<**String**> |  | [optional]
**include_deleted** | Option<**bool**> |  | [optional]
**page** | Option<**i32**> |  | [optional]
**page_size** | Option<**i32**> |  | [optional]
**total_pages** | Option<**i32**> |  | [optional]
**total_smart_plus_ads** | Option<**i32**> | Smart+ ads of the advertiser across all pages. | [optional]
**items** | Option<[**Vec<models::ListTikTokSmartPlusReviews200ResponseItemsInner>**](ListTikTokSmartPlusReviews200ResponseItemsInner.md)> |  | [optional]
**failed_smart_plus_ads** | Option<[**Vec<models::ListTikTokSmartPlusReviews200ResponseFailedSmartPlusAdsInner>**](ListTikTokSmartPlusReviews200ResponseFailedSmartPlusAdsInner.md)> | Smart+ ads of this page whose review TikTok refused on its own (for example an ad deleted on TikTok since the listing was cached). Zernio splits a refused batch in halves (at most 16 extra calls per page), so the other ads of the batch are still read; ads left unresolved by that cap carry the batch error. Empty when none. | [optional]
**incomplete** | Option<**bool**> | True when some Smart+ ads of this page could not be read because of TikTok's review quota. | [optional]
**pending_smart_plus_ad_ids** | Option<**Vec<String>**> | Smart+ ads of this page still to read. Empty when complete. | [optional]
**retry_after_seconds** | Option<**i32**> | Seconds to wait before reading this page again. Null when complete. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


