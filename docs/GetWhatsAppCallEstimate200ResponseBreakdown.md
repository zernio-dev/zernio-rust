# GetWhatsAppCallEstimate200ResponseBreakdown

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**meta_minutes** | Option<**i32**> |  | [optional]
**meta_cost_usd** | Option<**f64**> | Estimated Meta per-minute charge, billed by Meta directly to your WABA. Display only; not billed by Zernio. | [optional]
**telnyx_cost_usd** | Option<**f64**> |  | [optional]
**recording_cost_usd** | Option<**f64**> |  | [optional]
**billable_cost_usd** | Option<**f64**> | Estimated amount Zernio bills you = Telnyx leg + recording (excludes Meta). | [optional]
**total_cost_usd** | Option<**f64**> | Estimated full cost incl. the Meta portion you pay directly. Display only. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


