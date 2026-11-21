# UpdateGohighlevelSettingsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**relay_conversions** | Option<**bool**> | Relay GoHighLevel CRM events (new contacts, won opportunities, appointments, paid invoices and orders) as conversions with `source` `gohighlevel`. | [optional]
**write_back_attribution** | Option<**bool**> | Write each relayed conversion onto the `Zernio Conversions` custom field of the GoHighLevel contact. | [optional]
**report_to_ads** | Option<**bool**> | Also forward relayed conversions to the profile's ad platform destinations. Off stores them only. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


