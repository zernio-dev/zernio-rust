# WebhookPayloadPostPostPlatformsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **String** |  | 
**status** | **String** |  | 
**account_id** | Option<**String**> | SocialAccount id this platform target published through. Use it to route events by connected account (e.g. separate staging vs production endpoints). A post can span multiple accounts. | [optional]
**platform_post_id** | Option<**String**> |  | [optional]
**published_url** | Option<**String**> |  | [optional]
**error** | Option<**String**> |  | [optional]
**error_category** | Option<**ErrorCategory**> | Present when this target failed. Same taxonomy as `platforms[].errorCategory` on GET /v1/posts. (enum: auth_expired, user_content, user_abuse, account_issue, platform_rejected, platform_error, platform_rate_limit, quota_exhausted, system_error, unknown) | [optional]
**error_source** | Option<**ErrorSource**> | Present when this target failed. Who must act: user, platform or system (Zernio). (enum: user, platform, system) | [optional]
**platform_error** | Option<[**models::PostPlatformError**](PostPlatformError.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


