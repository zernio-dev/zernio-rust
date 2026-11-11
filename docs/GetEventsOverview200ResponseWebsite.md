# GetEventsOverview200ResponseWebsite

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**steps** | Option<[**Vec<models::GetEventsOverview200ResponseWebsiteStepsInner>**](GetEventsOverview200ResponseWebsiteStepsInner.md)> | The funnel: page views, product views, add to cart, checkouts and purchases today. | [optional]
**recovered** | Option<**i32**> | Purchases with ad consent for which no browser pixel fired, so only the server reported them. | [optional]
**conversions** | Option<**i32**> | Purchases today. | [optional]
**consented** | Option<**i32**> | Page views with ad storage consent. | [optional]
**visits** | Option<**i32**> | Page views today. | [optional]
**bots** | Option<**i32**> | Page views from bots. | [optional]
**server_platforms** | Option<**Vec<String>**> | Platforms of the forwarding rules that receive website events. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


