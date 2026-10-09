# ApiChangelogEntry

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Stable entry id; the same entry is never published twice. | 
**r#type** | **Type** | When `impact` is set, `breaking_change` means exactly `impact: action_required`. (enum: new_feature, breaking_change, improvement, deprecation, minor) | 
**impact** | Option<**Impact**> | What an integrator has to do, computed from the OpenAPI diff rather than from the prose. `action_required`: an existing call or parser can break (an operation, parameter or field removed, a field newly required, a type narrowed, an enum value removed, or authentication changed). `additive`: only new or looser things, existing integrations keep working. `none`: descriptions or examples only. Null on entries published before October 2026. (enum: none, additive, action_required, ) | 
**platforms** | **Vec<String>** | Platform and area slugs the entry is about: a platform (`instagram`, `facebook`, `threads`, `tiktok`, `x`, `linkedin`, `youtube`, `pinterest`, `reddit`, `bluesky`, `telegram`, `snapchat`, `whatsapp`, `discord`, `slack`, `google-business`, `imessage`), an ads platform (`meta-ads`, `google-ads`, `tiktok-ads`, `linkedin-ads`, `pinterest-ads`, `x-ads`) or an area (`ads`, `publishing`, `inbox`, `telephony`, `commerce`, `analytics`, `webhooks`, `general`). Filter with the `platform` query parameter. | 
**message** | **String** | The announcement, in Markdown. | 
**published_at** | **String** |  | 
**spec_version** | Option<**String**> | The `info.version` of the OpenAPI spec the entry describes, when known. | 
**url** | **String** | The entry on the docs changelog. | 
**changes** | [**models::ApiChangelogEntryChanges**](ApiChangelogEntryChanges.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


