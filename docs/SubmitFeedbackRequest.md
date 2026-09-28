# SubmitFeedbackRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **Type** | What kind of feedback this is. (enum: bug, missing_feature, docs, other) | 
**summary** | **String** | One line describing the problem or the missing capability. Also the dedup key. | 
**details** | Option<**String**> | Longer explanation: what you were trying to do, steps to reproduce, the use case. | [optional]
**endpoint** | Option<**String**> | The endpoint involved, e.g. `POST /v1/posts`. | [optional]
**request_id** | Option<**String**> | The `x-request-id` header of the failing response, if any. | [optional]
**expected** | Option<**String**> | What you expected to happen. | [optional]
**actual** | Option<**String**> | What actually happened, e.g. the error message. | [optional]
**agent** | Option<[**models::SubmitFeedbackRequestAgent**](SubmitFeedbackRequestAgent.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


