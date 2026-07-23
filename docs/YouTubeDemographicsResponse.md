# YouTubeDemographicsResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | Option<**bool**> |  | [optional]
**account_id** | Option<**String**> | The Zernio SocialAccount ID | [optional]
**platform** | Option<**String**> |  | [optional]
**video_id** | Option<**String**> | Present only when demographics are scoped to a single video | [optional]
**title** | Option<**String**> | Video title (video mode only) | [optional]
**published_at** | Option<**String**> | Video publish date (video mode only) | [optional]
**demographics** | Option<[**std::collections::HashMap<String, Vec<models::YouTubeDemographicsResponseDemographicsValueInner>>**](Vec.md)> | Object keyed by breakdown dimension (age, gender, country) | [optional]
**date_range** | Option<[**models::YouTubeDemographicsResponseDateRange**](YouTubeDemographicsResponseDateRange.md)> |  | [optional]
**provisional_since** | Option<[**String**](String.md)> | Present only when the range reaches into YouTube's ~3-day processing window: the first date whose numbers are provisional and may still be revised by YouTube. | [optional]
**note** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


