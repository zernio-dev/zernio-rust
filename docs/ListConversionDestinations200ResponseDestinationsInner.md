# ListConversionDestinations200ResponseDestinationsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Destination identifier. Meta: pixel ID. Google: conversion action resource name. LinkedIn: numeric conversion rule ID. OpenAI Ads: pixel wire id.  | [optional]
**name** | Option<**String**> |  | [optional]
**r#type** | Option<**String**> | Present when the platform locks event type to the destination (Google conversion actions, LinkedIn conversion rules).  | [optional]
**status** | Option<**Status**> |  (enum: active, inactive) | [optional]
**ad_account_id** | Option<**String**> | Set by adapters whose destinations are scoped to a specific ad account (LinkedIn). Pass back on subsequent CRUD calls.  | [optional]
**conversion_events** | Option<[**Vec<models::ListConversionDestinations200ResponseDestinationsInnerConversionEventsInner>**](ListConversionDestinations200ResponseDestinationsInnerConversionEventsInner.md)> | OpenAI Ads only: the conversion event settings wired to this pixel. Pass one's `id`, `eventType` or `name` as `promotedObject.customEventType` on a `goal: conversions` create (POST /v1/ads/create or POST /v1/ads/campaigns) to optimize for it. Without it, the account's most recently created `optimizable` event is used; when none is, the create returns 400.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


