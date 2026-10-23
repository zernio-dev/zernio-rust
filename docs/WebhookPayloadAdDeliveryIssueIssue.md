# WebhookPayloadAdDeliveryIssueIssue

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**raw** | **String** | Platform-native status string, forwarded verbatim (Meta `WITH_ISSUES`, TikTok `ADVERTISER_ACCOUNT_PUNISH`, LinkedIn `REMOVED`, ...). | 
**reasons** | [**Vec<models::WebhookPayloadAdReviewReviewReasonsInner>**](WebhookPayloadAdReviewReviewReasonsInner.md) | What the platform says is wrong. Meta reports it per campaign; other networks send no message today, so it is empty there. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


