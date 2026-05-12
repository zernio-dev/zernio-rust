# ListInboxComments200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**platform** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**account_username** | Option<**String**> |  | [optional]
**content** | Option<**String**> |  | [optional]
**picture** | Option<**String**> |  | [optional]
**permalink** | Option<**String**> |  | [optional]
**created_time** | Option<**String**> |  | [optional]
**comment_count** | Option<**i32**> |  | [optional]
**like_count** | Option<**i32**> |  | [optional]
**cid** | Option<**String**> | Bluesky content identifier | [optional]
**subreddit** | Option<**String**> | Reddit subreddit name | [optional]
**is_ad** | Option<**bool**> | True when this row is an ad (boosted/dark post). `platform` is then the placement (facebook = the Page dark post / instagram = the IG media), `id` is `{adId}:{placement}`, and the thread is at GET /v1/ads/{adId}/comments?placement={placement}. | [optional]
**ad_id** | Option<**String**> | Internal Zernio ad id — only on ad rows. | [optional]
**placement** | Option<**Placement**> | Which side of the ad this row's comments are on — only on ad rows. (enum: facebook, instagram) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


