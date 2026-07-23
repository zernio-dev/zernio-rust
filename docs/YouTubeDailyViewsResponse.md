# YouTubeDailyViewsResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | Option<**bool**> |  | [optional]
**video_id** | Option<**String**> | The YouTube video ID | [optional]
**duration_seconds** | Option<**i32**> | Video length in seconds (from YouTube contentDetails.duration) | [optional]
**date_range** | Option<[**models::YouTubeDailyViewsResponseDateRange**](YouTubeDailyViewsResponseDateRange.md)> |  | [optional]
**provisional_since** | Option<[**String**](String.md)> | Present only when the range reaches into YouTube's ~3-day processing window: the first date whose numbers are provisional and may still be revised by YouTube. | [optional]
**total_views** | Option<**i32**> | Sum of views across all days in the range | [optional]
**daily_views** | Option<[**Vec<models::YouTubeDailyViewsResponseDailyViewsInner>**](YouTubeDailyViewsResponseDailyViewsInner.md)> |  | [optional]
**last_synced_at** | Option<**String**> | When the data was last synced from YouTube | [optional]
**scope_status** | Option<[**models::YouTubeDailyViewsResponseScopeStatus**](YouTubeDailyViewsResponseScopeStatus.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


