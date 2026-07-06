# SendSmsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**from** | **String** | One of your SMS-enabled numbers (E.164; formatting is normalized). | 
**to** | **String** | Recipient number (E.164). | 
**text** | Option<**String**> | Message body. Required unless `mediaUrls` is set. Max 10 SMS segments (1530 GSM-7 or 670 unicode characters). | [optional]
**media_urls** | Option<**Vec<String>**> | Public media URLs to attach (sends as MMS). Max 10. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


