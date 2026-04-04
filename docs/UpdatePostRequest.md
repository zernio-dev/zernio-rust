# UpdatePostRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**content** | Option<**String**> |  | [optional]
**scheduled_for** | Option<**String**> |  | [optional]
**tiktok_settings** | Option<[**models::TikTokPlatformData**](TikTokPlatformData.md)> | Root-level TikTok settings applied to all TikTok platforms. Merged into each platform's platformSpecificData, with platform-specific settings taking precedence. | [optional]
**facebook_settings** | Option<[**models::FacebookPlatformData**](FacebookPlatformData.md)> | Root-level Facebook settings applied to all Facebook platforms. Merged into each platform's platformSpecificData, with platform-specific settings taking precedence. | [optional]
**recycling** | Option<[**models::RecyclingConfig**](RecyclingConfig.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


