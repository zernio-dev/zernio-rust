# WebhookPayloadAdStatusChangedError

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **String** | Platform-native error code, forwarded verbatim. For Meta this is `error_code` as a string. Use as the stable discriminator — `summary` and `message` are localized.  | 
**summary** | Option<**String**> | Short human-readable summary (Meta `error_summary`). Localized to the ad-account owner's Meta locale — display only, do not match on it.  | [optional]
**message** | Option<**String**> | Full human-readable error message (Meta `error_message`). Localized — display only.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


