# AdKeywordQuality

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**score** | Option<**i32**> | Quality Score, 1-10. | [optional]
**expected_ctr** | Option<**ExpectedCtr**> | How the click-through rate compares with other ads in the same position (`search_predicted_ctr`). (enum: BELOW_AVERAGE, AVERAGE, ABOVE_AVERAGE, ) | [optional]
**ad_relevance** | Option<**AdRelevance**> | How closely the ad matches the intent behind the search (`creative_quality_score`). (enum: BELOW_AVERAGE, AVERAGE, ABOVE_AVERAGE, ) | [optional]
**landing_page_experience** | Option<**LandingPageExperience**> | How relevant and useful the landing page is to people who click (`post_click_quality_score`). (enum: BELOW_AVERAGE, AVERAGE, ABOVE_AVERAGE, ) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


