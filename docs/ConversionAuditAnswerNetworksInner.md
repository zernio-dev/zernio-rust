# ConversionAuditAnswerNetworksInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **String** | Stable platform key (meta, google, tiktok, ...), as in `report.platforms`. | 
**name** | **String** | Short network name (Meta, Google, TikTok, ...). | 
**setup** | **Setup** | How the network gets its conversions: `verified`, `likely` or `possible` server path, `not-visible` (browser pixel, no server path visible), `not-firing` (installed, sent nothing), `configured` (tag manager only, never seen firing, not at risk) or `missing`. (enum: verified, likely, possible, not-visible, not-firing, configured, missing) | 
**leak_pct** | Option<**i32**> | Share of this network's conversions at risk, 0-100 (0 once a server path is verified). Null when the network has no working browser pixel to measure. | 
**loaded_by** | Option<**LoadedBy**> | `zernio-tag` when the pixel comes from the Zernio site tag's settings (it loads the pixel after consent) rather than from the page itself, on a scan that read the page source only. (enum: zernio-tag, ) | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


