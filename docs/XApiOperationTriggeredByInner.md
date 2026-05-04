# XApiOperationTriggeredByInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**method** | Option<**String**> | Zernio platform method name. | [optional]
**metering** | Option<**Metering**> | When the method actually bills the user:   * `always` — every call is metered   * `analytics_optin` — only when the X account has analytics enabled   * `inbox_optin` — only when the X account has inbox sync enabled   * `absorbed` — Zernio eats the cost, never billed  (enum: always, analytics_optin, inbox_optin, absorbed) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


