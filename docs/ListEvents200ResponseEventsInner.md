# ListEvents200ResponseEventsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**event_id** | Option<**String**> |  | [optional]
**event_name** | Option<**String**> |  | [optional]
**event_time** | Option<**String**> |  | [optional]
**received_at** | Option<**String**> |  | [optional]
**action_source** | Option<**String**> |  | [optional]
**value** | Option<**f64**> |  | [optional]
**currency** | Option<**String**> |  | [optional]
**source_url** | Option<**String**> | Origin, path and attribution parameters only. | [optional]
**utm** | Option<[**models::ListEvents200ResponseEventsInnerUtm**](ListEvents200ResponseEventsInnerUtm.md)> |  | [optional]
**zrn** | Option<**String**> | Ad ID from the `zrn` parameter Zernio adds to links of ads it creates. | [optional]
**click_ids** | Option<[**models::ListEvents200ResponseEventsInnerClickIds**](ListEvents200ResponseEventsInnerClickIds.md)> |  | [optional]
**destinations_sent** | Option<**i32**> | Destinations the event was forwarded to. | [optional]
**has_email** | Option<**bool**> |  | [optional]
**has_phone** | Option<**bool**> |  | [optional]
**has_external_id** | Option<**bool**> |  | [optional]
**ad** | Option<[**models::ListEvents200ResponseEventsInnerAd**](ListEvents200ResponseEventsInnerAd.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


