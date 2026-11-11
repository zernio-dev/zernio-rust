# GetEventsOverview200ResponseSourcesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**source** | Option<**String**> | Source id, such as `web`, `shopify` or `api` (which also covers `relay`). | [optional]
**label** | Option<**String**> | The source in plain words, such as `Shopify orders`. | [optional]
**state** | Option<**State**> | Always `on` for now: the source is sending events. (enum: on, available, connect) | [optional]
**events_today** | Option<**i32**> |  | [optional]
**last_seen_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


