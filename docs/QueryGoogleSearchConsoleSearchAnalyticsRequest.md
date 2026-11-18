# QueryGoogleSearchConsoleSearchAnalyticsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Zernio account ID of the Google Search Console connection. | 
**from_date** | Option<[**String**](String.md)> |  | [optional]
**to_date** | Option<[**String**](String.md)> |  | [optional]
**dimensions** | Option<**Vec<Dimensions>**> |  (enum: date, hour, query, page, country, device, searchAppearance, brandedClassification) | [optional]
**r#type** | Option<**Type**> | Which Google surface to read. Defaults to `web`. `webMultimodal` is Google Lens, Circle to Search and image uploads. (enum: web, image, video, news, discover, googleNews, webMultimodal) | [optional]
**dimension_filter_groups** | Option<[**Vec<models::QueryGoogleSearchConsoleSearchAnalyticsRequestDimensionFilterGroupsInner>**](QueryGoogleSearchConsoleSearchAnalyticsRequestDimensionFilterGroupsInner.md)> |  | [optional]
**aggregation_type** | Option<**AggregationType**> | byNewsShowcasePanel needs a NEWS_SHOWCASE searchAppearance filter and type discover or googleNews. (enum: auto, byPage, byProperty, byNewsShowcasePanel) | [optional]
**row_limit** | Option<**i32**> | Defaults to 1000. | [optional]
**start_row** | Option<**i32**> | Row offset for paging past `rowLimit`. | [optional]
**data_state** | Option<**DataState**> | `final` (default) leaves out the last two or three days; `all` includes them while Google is still filling them in; `hourly_all` is required with the `hour` dimension. (enum: final, all, hourly_all) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


