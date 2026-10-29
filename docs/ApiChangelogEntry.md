# ApiChangelogEntry

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Stable entry id; the same entry is never published twice. | 
**r#type** | **Type** | When `impact` is set, `breaking_change` means exactly `impact: action_required`. (enum: new_feature, breaking_change, improvement, deprecation, minor) | 
**impact** | Option<**Impact**> | What an integrator has to do, computed from the OpenAPI diff rather than the prose. Null on entries published before October 2026.  - `action_required`: an existing call or parser can break (an operation, parameter or field removed, a field newly required, a type narrowed, an enum value removed, or authentication changed). - `additive`: only new or looser things; existing integrations keep working. - `none`: descriptions or examples only.  (enum: none, additive, action_required, ) | 
**platforms** | **Vec<String>** | Platform and area slugs the entry is about. Filter with the `platform` query parameter.  - Platform: `instagram`, `facebook`, `threads`, `tiktok`, `x`, `linkedin`, `youtube`, `pinterest`, `reddit`, `bluesky`, `telegram`, `snapchat`, `whatsapp`, `discord`, `slack`, `google-business`, `imessage`. - Ads platform: `meta-ads`, `google-ads`, `tiktok-ads`, `linkedin-ads`, `pinterest-ads`, `x-ads`. - Area: `ads`, `publishing`, `inbox`, `telephony`, `commerce`, `analytics`, `webhooks`, `general`.  | 
**title** | Option<**String**> | The change in a few words, for example `Delete inbox conversations`. Null on older entries. | 
**summary** | Option<**String**> | One or two plain sentences on what changed and why it matters. Null when `title` is. | 
**message** | **String** | The details in Markdown: endpoints, fields and how to use them. | 
**published_at** | **String** |  | 
**spec_version** | Option<**String**> | The `info.version` of the OpenAPI spec the entry describes, when known. | 
**url** | **String** | The entry on the docs changelog. | 
**changes** | [**models::ApiChangelogEntryChanges**](ApiChangelogEntryChanges.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


