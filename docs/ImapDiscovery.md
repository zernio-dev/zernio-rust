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
**host_replacements** | Option<[**Vec<models::ImapDiscoveryHostReplacementsInner>**](ImapDiscoveryHostReplacementsInner.md)> | Server names discovery swapped for the name the server certificate is issued for, as on shared hosting where mail.<domain> has no certificate of its own. Present on the imap route. | [optional]
**reconnect_cause** | Option<**String**> |  | [optional]
**reason** | Option<**String**> |  | [optional]
**unsupported_reason** | Option<**UnsupportedReason**> | Why an `unsupported` route cannot connect:  - `proton_requires_bridge`: Proton Mail only works through its local bridge. - `forwarding_only`: the domain forwards mail (Cloudflare Email Routing) and stores none, so connect the mailbox it forwards to. - `domain_typo`: the domain takes no mail and looks like a mistyped consumer domain. `suggestedEmail` has the likely address. - `no_mail_domain`: the domain has no MX and no address, so it cannot receive email.  (enum: proton_requires_bridge, forwarding_only, domain_typo, no_mail_domain, ) | [optional]
**suggested_email** | Option<**String**> | With unsupportedReason domain_typo: the address the user most likely meant, such as ana7275@gmail.com for ana@7275gmail.com. Run discovery again with it once the user confirms. | [optional]
**app_password_fallback** | Option<**serde_json::Value**> | Google only: Gmail over IMAP with an app password, for accounts whose admin blocks Google sign-in for other apps. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


