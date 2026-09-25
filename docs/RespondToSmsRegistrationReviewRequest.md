# RespondToSmsRegistrationReviewRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**note** | Option<**String**> | Answer for the reviewer. Required when no files are sent. | [optional]
**files** | Option<**Vec<String>**> | Hosted document URLs returned by POST /v1/sms/opt-in-proof. | [optional]
**request_id** | Option<**String**> | The `reviewRequest.id` you are answering. When it no longer matches the open request the reply is refused with 409. | [optional]
**answers** | Option<[**Vec<models::RespondToSmsRegistrationReviewRequestAnswersInner>**](RespondToSmsRegistrationReviewRequestAnswersInner.md)> | One answer per point of the open `reviewRequest`, each point at most once. Required (every point) when the request has points; a missing, repeated or unknown point is a 400 naming the point ids. At most 10 files per reply. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


