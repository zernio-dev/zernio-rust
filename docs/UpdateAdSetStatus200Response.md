# UpdateAdSetStatus200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | Option<**Status**> | The status written to the ad set switch (enum: active, paused) | [optional]
**updated** | Option<**i32**> | Number of ads whose own stored status changed too. 0 is normal on a resume whose ads are all awaiting the platform. | [optional]
**skipped** | Option<**i32**> | Number of ads whose own status was left as it was | [optional]
**skipped_reasons** | Option<**Vec<String>**> | Why each group of ads was skipped (for example \"2 ads already switched off\", read from each ad's own switch) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


