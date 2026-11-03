# WebhookPayloadAdReviewReview

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **Status** |  (enum: approved, rejected) | 
**raw** | **String** | Platform-native status string, forwarded verbatim (Meta `ACTIVE` / `DISAPPROVED`, TikTok `DISABLE`, ...). | 
**reasons** | [**Vec<models::WebhookPayloadAdReviewReviewReasonsInner>**](WebhookPayloadAdReviewReviewReasonsInner.md) | Why the platform rejected the ad, when it says. Always empty on `approved`. Pinterest, LinkedIn and Reddit send their own reasons, X sends none, and most other networks only return a generic message. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


