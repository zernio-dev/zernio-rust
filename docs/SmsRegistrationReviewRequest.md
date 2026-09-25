# SmsRegistrationReviewRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Changes with every request. Send it back as `requestId` when answering, so a reply to a replaced request is refused (409) instead of filed under the new points. | [optional]
**intro** | Option<**String**> | Context from the reviewer, e.g. what was already fixed on our side. | [optional]
**points** | Option<[**Vec<models::SmsRegistrationReviewRequestPointsInner>**](SmsRegistrationReviewRequestPointsInner.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


