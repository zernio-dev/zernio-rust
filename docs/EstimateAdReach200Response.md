# EstimateAdReach200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**available** | **bool** | Whether a pre-flight estimate is available on this platform. False for Google and TikTok. | 
**lower** | Option<**i32**> | Lower bound of the estimated reachable audience. Present only when available. | [optional]
**upper** | Option<**i32**> | Upper bound of the estimated reachable audience. Present only when available. | [optional]
**daily** | Option<**i32**> | Optional estimated daily reach/results at the given budget, when the platform returns it. | [optional]
**currency** | Option<**String**> | Currency of any monetary fields in the estimate, when applicable. | [optional]
**estimate_ready** | Option<**bool**> | Meta only. False when Meta is still computing the estimate (the audience is too new); retry shortly. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


