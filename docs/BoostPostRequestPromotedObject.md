# BoostPostRequestPromotedObject

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**pixel_id** | Option<**String**> | Meta Pixel id, or TikTok Pixel (numeric id or the alphanumeric pixel code from Events Manager, resolved for you). | [optional]
**custom_event_type** | Option<**String**> | Meta: standard pixel event (PURCHASE, LEAD, ...) or OTHER with customEventStr. TikTok: optimization_event code (e.g. ON_WEB_ORDER, SHOPPING, FORM) or the exact event name shown in Events Manager, resolved to its code; the event must already exist on that pixel. | [optional]
**custom_event_str** | Option<**String**> | Meta only. Pixel custom event name as it appears in Events Manager; requires customEventType OTHER. | [optional]
**custom_conversion_id** | Option<**String**> | Meta only. Custom Conversion to optimize against, instead of pixelId + customEventType. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


