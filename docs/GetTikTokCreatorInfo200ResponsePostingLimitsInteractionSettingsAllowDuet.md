# GetTikTokCreatorInfo200ResponsePostingLimitsInteractionSettingsAllowDuet

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | Option<**bool**> | Whether the creator permits this interaction. False means they disabled it in the TikTok app. This is availability, never the value the user selected. | [optional]
**required** | Option<**bool**> | Whether tiktokSettings.allow_duet must be supplied when creating a post. Always true, because TikTok forbids defaulting it. | [optional]
**default** | Option<**bool**> | Initial value a post composer should render. A UI seed only, never applied server-side when the field is omitted. | [optional]
**label** | Option<**String**> | Human-readable toggle label. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


