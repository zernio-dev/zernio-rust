# ListAdsInstagramAccounts200ResponseAccountsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ig_user_id** | **String** | Instagram identity ID. | 
**username** | **String** | Instagram username; empty when Meta does not expose it. | 
**profile_picture_url** | Option<**String**> | Profile picture URL when available. | [optional]
**is_page_backed** | **bool** | Whether this is a Page-backed Instagram identity. | 
**source** | **Source** | Discovery source; Page linkage also uses page_backed. business_partner is a partner asset shared with the ad account's business; promote_pages is linked to a Page the ad account promotes. (enum: ad_account, page_backed, business, business_partner, promote_pages) | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


