# TrackingTag

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Platform-native tag id, the `{tagId}` of the per-tag routes. Meta: numeric pixel id, as a string. OpenAI: the pixel resource id. Google Ads: the 10-digit customer id (one Google tag per account). | 
**site_tag_id** | Option<**String**> | The id the on-site code carries. Equals `id` on Meta; differs on platforms with separate API and site ids (OpenAI `pixel_id`, Google `AW-...` conversion id, the manager's under cross-account conversion tracking). | [optional]
**events** | Option<[**Vec<models::TrackingTagEvent>**](TrackingTagEvent.md)> | Platforms where each conversion is its own object: the tag's conversion events, with the id a site sends for each. | [optional]
**name** | **String** |  | 
**platform** | **Platform** |  (enum: metaads, openaiads, tiktokads, googleads, xads, linkedinads, pinterestads, whopads) | 
**kind** | **Kind** | Platform-native flavor of the tag (Meta: `pixel`). (enum: pixel, tag, insight_tag) | 
**status** | **Status** | `inactive` when the platform reports the tag as broken/unavailable. (enum: active, inactive) | 
**code** | Option<**String**> | The base-code `<script>` snippet to install on the site, including the page-view call. Populated by `getTrackingTag`, omitted from the list view.  | [optional]
**last_fired_time** | Option<**i32**> | Unix seconds of the last event the tag received, or `null` if it never fired. The practical \"is it installed and working\" signal.  | [optional]
**is_unavailable** | Option<**bool**> | Whether the tag is in a broken/unavailable state (Meta `is_unavailable`). | [optional]
**installed** | Option<**bool**> | Convenience flag derived from `lastFiredTime`: has the tag ever fired. | [optional]
**creation_time** | Option<**i32**> | Unix seconds the tag was created. | [optional]
**automatic_matching_fields** | Option<**Vec<AutomaticMatchingFields>**> | Customer data the tag matches automatically, where the platform reports it (Pinterest automatic enhanced match). (enum: em, ph, fn, ln, ge, db, ct, st, zp, country, external_id) | [optional]
**owner_business_id** | Option<**String**> | Business Manager id that owns the tag, or `null` when the tag lives on a personal (non-BM) ad account. Such tags can't be shared with other ad accounts.  | [optional]
**owner_ad_account_id** | Option<**String**> | Ad account id (`act_...`) that owns the tag, when reported. | [optional]
**auto_tagging** | Option<**bool**> | Google Ads: whether gclid auto-tagging is on for the ad account (needed to attribute conversions to clicks). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


