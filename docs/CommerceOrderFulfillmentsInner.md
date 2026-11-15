# CommerceOrderFulfillmentsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | The shipment (fulfillment) id. Entries of one shipment with several tracking numbers share it. | [optional]
**carrier_name** | Option<**String**> |  | [optional]
**tracking_number** | Option<**String**> |  | [optional]
**tracking_url** | Option<**String**> |  | [optional]
**delivery_status** | Option<**DeliveryStatus**> | Where the shipment is. pending means no carrier scan yet. Null when the platform has no delivery tracking for it. Shopify only knows it when the carrier sends tracking events. (enum: pending, in_transit, delayed, out_for_delivery, ready_for_pickup, attempted_delivery, delivered, failed, cancelled, ) | [optional]
**platform_delivery_status** | Option<**String**> | The platform's raw value, e.g. Shopify ATTEMPTED_DELIVERY. | [optional]
**estimated_delivery_at** | Option<**String**> |  | [optional]
**in_transit_at** | Option<**String**> |  | [optional]
**delivered_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


