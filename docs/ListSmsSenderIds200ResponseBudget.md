# ListSmsSenderIds200ResponseBudget

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cap** | Option<**i32**> | Daily message cap (raisable via `/v1/sms/sender-ids/limit-request`). | [optional]
**used_today** | Option<**i32**> | Messages already counted against today's cap. | [optional]
**level** | Option<**i32**> | Cap tier (Level 1 = 500/day). | [optional]
**pending_request** | Option<[**models::ListSmsSenderIds200ResponseBudgetPendingRequest**](ListSmsSenderIds200ResponseBudgetPendingRequest.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


