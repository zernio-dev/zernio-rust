# AdTracking

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**pixel_id** | Option<**String**> | Meta Pixel ID to attach for offsite-conversion measurement. | [optional]
**url_tags** | Option<[**Vec<models::UpdateAdTrackingTagsRequestUrlTagsInner>**](UpdateAdTrackingTagsRequestUrlTagsInner.md)> | Click-URL params. Meta: stored on the creative as `url_tags` and returned by GET /v1/ads/{adId}/tracking-tags. App-promotion linkUrl stays byte-identical to promotedObject.objectStoreUrl. Meta dynamic macros ({{ad.id}}, {{campaign.id}}, {{placement}}, ...) are sent through unescaped so Meta expands them; every other character is percent-encoded. ChatGPT (OpenAI): the same encoding, with OpenAI's macros `{campaign_id}`, `{ad_group_id}`, `{ad_id}` and `{oppref}` (click id) passed through raw. OpenAI expands macros here, not inside `linkUrl`. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


