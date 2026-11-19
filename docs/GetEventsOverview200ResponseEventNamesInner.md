# GetEventsOverview200ResponseEventNamesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**event_name** | Option<**String**> |  | [optional]
**server_sources** | Option<**Vec<String>**> | The server sources that reported it (api, stripe, shopify...). Empty when only the website did. | [optional]
**from_website** | Option<**bool**> | The website tag reported it. | [optional]
**website_today** | Option<**i32**> | Website copies today. | [optional]
**server_today** | Option<**i32**> | Server copies today. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


