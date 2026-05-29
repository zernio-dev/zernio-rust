# ListWhatsAppCalls200ResponseCallsInnerBilling

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**meta_cost_usd** | Option<**f64**> | Meta per-minute charge, billed by Meta directly to your WABA. Display only; not billed by Zernio. | [optional]
**telnyx_cost_usd** | Option<**f64**> |  | [optional]
**recording_cost_usd** | Option<**f64**> |  | [optional]
**billable_cost_usd** | Option<**f64**> | Amount Zernio bills you = Telnyx leg + recording (excludes Meta). | [optional]
**total_cost_usd** | Option<**f64**> | Full cost incl. the Meta portion you pay directly. Display only. | [optional]
**currency** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


