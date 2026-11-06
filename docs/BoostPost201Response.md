# BoostPost201Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ad** | Option<[**models::Ad**](Ad.md)> |  | [optional]
**message** | Option<**String**> |  | [optional]
**instagram_video_fallback** | Option<[**models::InstagramVideoFallback**](InstagramVideoFallback.md)> |  | [optional]
**recovered_writes** | Option<[**Vec<models::MetaRecoveredWritesInner>**](MetaRecoveredWritesInner.md)> | Meta only, present only when needed. Every object this request did not get confirmed by its first POST: found by name after Meta lost or failed its answer (`adopted`), or created by a second POST after a Meta 5xx (`repostedAfter`).  A re-POSTed object may have a twin from the first POST that Meta wrote late: check its parent for a duplicate name. Send `retryOnServerError: false` to never re-POST.  | [optional]
**warnings** | Option<**Vec<String>**> | Human-readable notes about the boost.  - **With instagramVideoFallback:** one line saying how the Instagram video was boosted. - **`activation_failed:` (Meta):** Meta refused the final switch to ACTIVE of the campaign, ad set or ad this boost created. Nothing was deleted and `message` says not everything is ACTIVE. - **`activation_failed:` content:** names what was kept PAUSED and what was switched ACTIVE, and quotes Meta's error and the status calls that switch the PAUSED ones on later. - **`replayed_paused:`:** a retry without Idempotency-Key inside the 10-minute dedup window found the stored ad PAUSED although it asks for ACTIVE. Carries the same status calls.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


