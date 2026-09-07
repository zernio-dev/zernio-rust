# CreateTrackingTagRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ad_account_id** | **String** | Meta ad account id, e.g. `act_123456789`. Required by this endpoint but ignored for OpenAI Ads. | 
**name** | **String** |  | 
**default_event_type** | Option<**DefaultEventType**> | OpenAI Ads only (ignored by Meta). When set, also provisions a standard conversion event setting wired to the new pixel, so `goal: conversions` ad creates on `POST /v1/ads/create` have an event to reference immediately. (enum: order_created, lead_created, items_added, contents_viewed, checkout_started, registration_completed, subscription_created, trial_started, appointment_scheduled, page_viewed, app_installed, app_opened) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


