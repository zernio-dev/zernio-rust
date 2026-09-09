# AdTracking

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**pixel_id** | Option<**String**> | Meta Pixel ID to attach for offsite-conversion measurement. | [optional]
**url_tags** | Option<[**Vec<models::UpdateAdTrackingTagsRequestUrlTagsInner>**](UpdateAdTrackingTagsRequestUrlTagsInner.md)> | Click-URL params stored on the creative as `url_tags` and returned by GET /v1/ads/{adId}/tracking-tags. App-promotion linkUrl stays byte-identical to promotedObject.objectStoreUrl. Meta dynamic macros ({{ad.id}}, {{campaign.id}}, {{placement}}, ...) are sent through unescaped so Meta expands them; every other character is percent-encoded. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


