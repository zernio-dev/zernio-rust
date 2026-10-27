# BoostPost201Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ad** | Option<[**models::Ad**](Ad.md)> |  | [optional]
**message** | Option<**String**> |  | [optional]
**instagram_video_fallback** | Option<[**models::InstagramVideoFallback**](InstagramVideoFallback.md)> |  | [optional]
**warnings** | Option<**Vec<String>**> | Present with instagramVideoFallback: one human-readable line saying how the Instagram video was boosted. On Meta also present, as an entry starting with `activation_failed:`, when Meta refused the final switch to ACTIVE of the campaign, ad set or ad this boost created: nothing was deleted, `message` says not everything is ACTIVE, and the entry names what was kept PAUSED and what was switched ACTIVE, and quotes Meta's error and the status calls that switch the PAUSED ones on later. A retry without Idempotency-Key inside the 10-minute dedup window that finds the stored ad PAUSED although it asks for ACTIVE gets a `replayed_paused:` entry with the same status calls instead. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


