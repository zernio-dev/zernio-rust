# ConversionAuditReportPlatformsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **String** | Stable platform key (meta, google, tiktok, ...). | 
**name** | **String** | Human-readable platform name. | 
**browser_pixel** | **bool** | Whether a browser pixel for this platform was found. | 
**server_side** | **bool** | True only when a server-side path is proven: visible from the page, or verified through the Zernio account behind the site tag. | 
**relayed_by** | Option<**RelayedBy**> | The only server path seen is the Zernio site tag relay; `serverSideVerified` says whether its delivery to this platform is proven. (enum: zernio-tag) | [optional]
**loaded_by** | Option<**LoadedBy**> | On a scan that read the page source only: the pixel comes from the Zernio site tag's settings, which load it after consent, not from the page. Its ids are not reported. (enum: zernio-tag) | [optional]
**server_side_verified** | Option<**bool**> | The Zernio site tag on the page belongs to an account whose destination for this platform accepted the site's events in the last 7 days. | [optional]
**server_tool** | Option<**String**> | A third-party server-side tool installed on the site that may already send this platform's events (Elevar, Littledata, Stape), when its status is `likely`. Which platforms the tool feeds is not visible from the page. | [optional]
**status** | **Status** | `good`: server-side. `warn`: browser-only (the leak). `missing`: not tracked. `not-firing`: installed but sent nothing during a full visit. `configured`: only in a Google Tag Manager container and not seen firing on a visit where silence proves nothing, so not counted as tracked. (enum: good, warn, missing, not-firing, configured) | 
**estimated_loss_browser_only** | **f64** | Share of conversions typically lost when this platform runs browser-only, 0-1. | 
**note** | **String** | Short explanation of the finding. | 
**ids** | Option<**Vec<String>**> | Pixel or tag ids found for this platform. | [optional]
**events** | Option<**Vec<String>**> | Standard events called in the page or its tag-manager containers. | [optional]
**fix_steps** | Option<**Vec<String>**> | Steps to fix this platform's tracking. | [optional]
**fired** | Option<**Fired**> | Rendered scans: `after-consent` when the pixel fired only once the scan accepted the cookie banner. (enum: before-consent, after-consent) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


