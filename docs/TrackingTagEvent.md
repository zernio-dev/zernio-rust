# TrackingTagEvent

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Platform-native event id, the `{eventId}` of the per-event routes. | 
**name** | **String** |  | 
**r#type** | Option<**String**> | Platform event type or category. | [optional]
**site_event** | Option<**SiteEvent**> | The neutral site event this conversion is fired for, when it maps to one. (enum: page_view, view_content, add_to_cart, search, initiate_checkout, add_payment_info, purchase) | [optional]
**site_event_id** | Option<**String**> | What the site sends to fire this event (Google conversion label, LinkedIn conversion rule id, X `tw-` event id). | [optional]
**status** | Option<**String**> |  | [optional]
**default_value** | Option<**f64**> |  | [optional]
**currency** | Option<**String**> |  | [optional]
**click_window_days** | Option<**i32**> |  | [optional]
**view_window_days** | Option<**i32**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


