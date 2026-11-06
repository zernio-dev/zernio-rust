# CreateStandaloneAd201ResponseOneOf1

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ads** | Option<[**Vec<models::Ad>**](Ad.md)> |  | [optional]
**platform_campaign_id** | Option<**String**> |  | [optional]
**platform_ad_set_id** | Option<**String**> |  | [optional]
**applied_defaults** | Option<[**models::AdAppliedDefaults**](AdAppliedDefaults.md)> |  | [optional]
**message** | Option<**String**> |  | [optional]
**recovered_writes** | Option<[**Vec<models::MetaRecoveredWritesInner>**](MetaRecoveredWritesInner.md)> | Meta only, present only when needed. Every object this request did not get confirmed by its first POST: found by name after Meta lost or failed its answer (`adopted`), or created by a second POST after a Meta 5xx (`repostedAfter`).  A re-POSTed object may have a twin from the first POST that Meta wrote late: check its parent for a duplicate name. Send `retryOnServerError: false` to never re-POST.  | [optional]
**warnings** | Option<**Vec<String>**> | Meta only, present only when needed.  An `activation_failed:` entry means Meta refused the final switch to ACTIVE for the ads it names (or for their ad set or campaign). The entry names what was kept PAUSED and what was switched ACTIVE, and quotes Meta's error and the status calls that switch the PAUSED ones on later.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


