# GetAd200ResponseDarkPost

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | Option<**Platform**> |  (enum: facebook) | [optional]
**platform_post_id** | Option<**String**> | The dark post id, `{pageId}_{postId}`. | [optional]
**page_id** | Option<**String**> |  | [optional]
**is_dark_post** | Option<**bool**> | Always true. | [optional]
**ad_id** | Option<**String**> | Always null: Meta exposes no link from a placement dark post to its ad. | [optional]
**account_id** | Option<**String**> | Zernio Meta Ads account id for the Page, null when none is connected. | [optional]
**facebook_account_id** | Option<**String**> | Zernio Facebook account id of the Page. | [optional]
**platform_ad_account_ids** | Option<**Vec<String>**> | Meta ad accounts (`act_...`) with synced ads on this Page. | [optional]
**first_seen_at** | Option<**String**> |  | [optional]
**last_activity_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


