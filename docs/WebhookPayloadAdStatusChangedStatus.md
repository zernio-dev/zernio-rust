# WebhookPayloadAdStatusChangedStatus

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**raw** | **String** | Platform-native status string, forwarded verbatim. For Meta this is `status_name` from `in_process_ad_objects` (e.g. `ACTIVE`, `PAUSED`, `PENDING_REVIEW`, `ARCHIVED`, `DELETED`, `DISAPPROVED`), or `WITH_ISSUES` when sourced from `with_issues_ad_objects`. Not constrained by an `enum` — Meta may add new values.  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


