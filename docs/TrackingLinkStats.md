# TrackingLinkStats

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**from_date** | [**String**](String.md) |  | 
**to_date** | [**String**](String.md) |  | 
**clicks** | **i32** | Human clicks in the range. | 
**conversions** | **i32** | Conversions still counted whose time falls in the range. | 
**conversion_rate** | Option<**f64**> | Conversions per click. Null without clicks. | 
**revenue** | [**Vec<models::TrackingLinkStatsRevenueInner>**](TrackingLinkStatsRevenueInner.md) | The conversions' value summed per currency, most conversions first. | 
**destinations** | [**Vec<models::TrackingLinkStatsDestinationsInner>**](TrackingLinkStatsDestinationsInner.md) | The link's current destinations, each with its clicks in the range. | 
**former_destination_clicks** | **i32** | Clicks on destinations the link no longer has (an edited or removed URL). | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


