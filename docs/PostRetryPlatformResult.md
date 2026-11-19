# PostRetryPlatformResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **String** | Platform slug, matching `post.platforms[].platform`. | 
**account_id** | **String** | Account id of this platform. | 
**retried** | **bool** | Whether this request retried the platform. False for a platform that had already published, or one left out of `platforms`. | 
**status** | **String** | Status after the retry: pending, processing, published, failed, cancelled, uploading. | 
**error** | Option<**String**> | Failure message for this platform, or null when it did not fail. | 
**error_category** | Option<**String**> | Stable failure category (for example `auth_expired`, `account_issue`, `user_content`, `platform_error`), or null. | 
**error_source** | Option<**String**> | Who caused the failure (`user`, `platform` or `system`), or null. | 
**platform_error_code** | Option<**i32**> | Error code returned by the platform, when it sent one. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


