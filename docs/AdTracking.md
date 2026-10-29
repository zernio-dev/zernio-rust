# AdTracking

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**pixel_id** | Option<**String**> | Meta Pixel ID to attach for offsite-conversion measurement, or the Reddit pixel of the new ad group. | [optional]
**url_tags** | Option<[**Vec<models::UpdateAdTrackingTagsRequestUrlTagsInner>**](UpdateAdTrackingTagsRequestUrlTagsInner.md)> | Click-URL params.  - Meta: stored on the creative as `url_tags` and returned by GET /v1/ads/{adId}/tracking-tags. Dynamic macros ({{ad.id}}, {{campaign.id}}, {{placement}}, ...) are sent through unescaped so Meta expands them; every other character is percent-encoded. App-promotion linkUrl stays byte-identical to promotedObject.objectStoreUrl. - ChatGPT (OpenAI): the same encoding, with OpenAI's macros `{campaign_id}`, `{ad_group_id}`, `{ad_id}` and `{oppref}` (click id) passed through raw. OpenAI expands macros here, not inside `linkUrl`.  | [optional]
**zernio_tag** | Option<**bool**> | POST /v1/ads/create on Meta and Google only. Opt-in: set `true` and the ad carries `zrn=<platform ad id>` on its landing URL, so orders and events tied to the landing URL map back to the ad.  - **Meta:** `{ key: zrn, value: '{{ad.id}}' }` is appended after your `urlTags`, which are sent unchanged; a `zrn` key you send yourself is kept. Skipped for lead forms, call ads, `existingCreativeId` and app promotion. - **Google (Display and Search):** the ad's `final_url_suffix` is set to `zrn={creative}` only when the ad inherits no suffix from its ad group, campaign or account. Otherwise the ad is left untouched (your suffix keeps applying) and attribution uses the click's `gclid`. - If the inherited suffix cannot be read or Google rejects the tag, the ad is created untagged.  Existing ads are never changed. Omitted or `false` creates the ad with no Zernio tag.  | [optional][default to false]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


