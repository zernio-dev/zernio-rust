# ImapDiscovery

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | Option<**String**> |  | [optional]
**route** | Option<**Route**> |  (enum: imap, google_oauth, microsoft_oauth, unsupported) | [optional]
**provider** | Option<[**models::ImapDiscoveryProvider**](ImapDiscoveryProvider.md)> |  | [optional]
**source** | Option<**Source**> |  (enum: preset, mx, autoconfig, ispdb, srv, probe, none) | [optional]
**confidence** | Option<**Confidence**> | low when only a probe answered: show the settings for the user to check. (enum: high, medium, low) | [optional]
**imap** | Option<[**models::ImapDiscoveryImap**](ImapDiscoveryImap.md)> |  | [optional]
**smtp** | Option<[**models::ImapDiscoverySmtp**](ImapDiscoverySmtp.md)> |  | [optional]
**auth** | Option<[**models::ImapDiscoveryAuth**](ImapDiscoveryAuth.md)> |  | [optional]
**preflight** | Option<[**Vec<models::ImapDiscoveryPreflightInner>**](ImapDiscoveryPreflightInner.md)> | What to switch on at the provider first, such as IMAP access on GMX or Yandex. | [optional]
**reconnect_cause** | Option<**String**> |  | [optional]
**reason** | Option<**String**> |  | [optional]
**unsupported_reason** | Option<**UnsupportedReason**> |  (enum: proton_requires_bridge, ) | [optional]
**app_password_fallback** | Option<**serde_json::Value**> | Google only: Gmail over IMAP with an app password, for accounts whose admin blocks Google sign-in for other apps. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


