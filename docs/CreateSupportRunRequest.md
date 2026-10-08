# CreateSupportRunRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **String** | The question. Leading and trailing whitespace is trimmed. | 
**thread_id** | Option<**String**> | Continue this thread. The thread must have a run started by your team, and no run in progress. | [optional]
**context** | Option<[**models::CreateSupportRunRequestContext**](CreateSupportRunRequestContext.md)> |  | [optional]
**max_cost_usd** | Option<**f64**> | Cost cap for this run, in USD. The run stops at the cap and bills at most this amount. | [optional][default to 3]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


