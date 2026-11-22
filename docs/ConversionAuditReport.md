# ConversionAuditReport

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **String** | The normalized URL that was scanned. | 
**domain** | **String** | The scanned host without `www.`. | 
**score** | **f64** | Conversion tracking score, 0-100. Higher means a more complete setup and less signal at risk. | 
**grade** | **Grade** | Letter grade for the score. (enum: A, B, C, D, F) | 
**score_range** | Option<[**models::ConversionAuditReportScoreRange**](ConversionAuditReportScoreRange.md)> |  | [optional]
**estimated_signal_loss_pct** | **f64** | Average share of conversions at risk on the networks with no visible server-side path, 0-100. | 
**platforms** | [**Vec<models::ConversionAuditReportPlatformsInner>**](ConversionAuditReportPlatformsInner.md) | One finding per ad platform the scan looked for. | 
**browser_only** | **bool** | True when every active platform is tracked browser-only. | 
**consent_manager** | Option<**String**> | Consent manager found on the page, or null. | 
**active_platform_count** | **i32** | How many ad platforms the scan found any tracking for. | 
**visibility** | **Visibility** | `full` = pixels were visible, `limited` = tags load dynamically so not all are visible, `none` = nothing found. (enum: full, limited, none) | 
**site_signals** | **Vec<String>** | Site tech recognized (Shopify, WooCommerce, ...). | 
**scan_mode** | Option<**ScanMode**> | `rendered` when a headless browser ran the page and its requests were checked, `static` for the page source only. (enum: static, rendered) | [optional]
**limitations** | Option<**Vec<String>**> | What this scan could not see. | [optional]
**checks** | Option<[**Vec<models::ConversionAuditReportChecksInner>**](ConversionAuditReportChecksInner.md)> | The scored checks behind `score`. | [optional]
**server_side** | Option<[**models::ConversionAuditReportServerSide**](ConversionAuditReportServerSide.md)> |  | [optional]
**consent** | Option<[**models::ConversionAuditReportConsent**](ConversionAuditReportConsent.md)> |  | [optional]
**consent_scan** | Option<[**models::ConversionAuditReportConsentScan**](ConversionAuditReportConsentScan.md)> |  | [optional]
**tag_managers** | Option<**Vec<String>**> |  | [optional]
**other_networks** | Option<[**Vec<models::ConversionAuditReportOtherNetworksInner>**](ConversionAuditReportOtherNetworksInner.md)> | Ad networks found that the score does not cover. `relaySupported` is true when Zernio can send them conversions. | [optional]
**other_networks_configured** | Option<[**Vec<models::ConversionAuditReportOtherNetworksInner>**](ConversionAuditReportOtherNetworksInner.md)> | Rendered scans: unscored ad networks found only in a Google Tag Manager container that the visit never saw load or send. Not counted in `otherNetworks`. | [optional]
**favicon_url** | Option<**String**> | The site's icon. Absent when the site was unreachable. | [optional]
**summary** | **String** | One-paragraph summary of the audit. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


