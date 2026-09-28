# CreateTrackingTagEventRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ad_account_id** | Option<**String**> | Scopes the lookup on platforms whose tag ids live inside an ad account. | [optional]
**name** | **String** |  | 
**r#type** | Option<**String**> | The platform's own event type enum value (e.g. `PURCHASE`). | [optional]
**site_event** | Option<**SiteEvent**> | Neutral alternative to `type`, mapped to the platform's closest type. (enum: page_view, view_content, add_to_cart, search, initiate_checkout, add_payment_info, purchase) | [optional]
**enabled** | Option<**bool**> |  | [optional]
**default_value** | Option<**f64**> |  | [optional]
**currency** | Option<**String**> | ISO 4217 code. | [optional]
**click_window_days** | Option<**i32**> |  | [optional]
**view_window_days** | Option<**i32**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


