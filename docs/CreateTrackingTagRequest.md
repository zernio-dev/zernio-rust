# CreateTrackingTagRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ad_account_id** | **String** | Meta ad account id, e.g. `act_123456789`. Required by this endpoint but ignored for OpenAI Ads. | 
**name** | **String** |  | 
**default_event_type** | Option<**DefaultEventType**> | OpenAI Ads only (ignored by Meta). When set, also provisions a standard conversion event setting wired to the new pixel, so `goal: conversions` ad creates on `POST /v1/ads/create` have an event to reference immediately. (enum: order_created, lead_created, items_added, contents_viewed, checkout_started, registration_completed, subscription_created, trial_started, appointment_scheduled, page_viewed, app_installed, app_opened) | [optional]
**automatic_matching_fields** | Option<**Vec<AutomaticMatchingFields>**> | Pinterest only (400 elsewhere). Customer data the new tag matches automatically (automatic enhanced match): `em` email, `ph` phone, `fn`/`ln` name, `ge` gender, `db` date of birth, `ct`/`st`/`zp`/`country` location, `external_id`. Pinterest has one switch for the name and one for the location, so `fn` turns on `ln` too and any location code turns on all four. (enum: em, ph, fn, ln, ge, db, ct, st, zp, country, external_id) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


