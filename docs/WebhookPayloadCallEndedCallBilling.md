# WebhookPayloadCallEndedCallBilling

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**meta_cost_usd** | Option<**f64**> | Meta per-minute charge. Billed by Meta DIRECTLY to your WhatsApp Business Account payment method (your separate Meta invoice). Zernio does NOT charge this. Display only. | [optional]
**telnyx_cost_usd** | Option<**f64**> |  | [optional]
**recording_cost_usd** | Option<**f64**> |  | [optional]
**billable_cost_usd** | Option<**f64**> | The amount Zernio bills you = Telnyx leg + recording. Excludes Meta (billed by Meta directly). | [optional]
**total_cost_usd** | Option<**f64**> | Full economic cost incl. the Meta portion you pay directly (Meta + Telnyx + recording). Display only, not the Zernio-billed amount. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


