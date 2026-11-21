# UpdateGohighlevelSettingsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**relay_conversions** | Option<**bool**> | Relay GoHighLevel CRM events (new contacts, won opportunities, appointments, paid invoices and orders) as conversions with `source` `gohighlevel`. | [optional]
**write_back_attribution** | Option<**bool**> | Write each relayed conversion onto the `Zernio Conversions` custom field of the GoHighLevel contact. | [optional]
**report_to_ads** | Option<**bool**> | Also forward relayed conversions to the profile's ad platform destinations. Off stores them only. | [optional]
**sync_contacts** | Option<**bool**> | Match inbox contacts to HighLevel contacts (phone, then email) and create the ones that do not exist. | [optional]
**log_messages** | Option<**bool**> | Log inbox messages from every channel on the matched HighLevel contact, one note per channel and UTC day. | [optional]
**log_delivery_status** | Option<**bool**> | Mark sent, delivered, read and failed on logged outgoing messages. | [optional]
**sync_ad_leads** | Option<**bool**> | Create or update a HighLevel contact for every lead from the profile's ad network lead forms (Meta, TikTok, LinkedIn, Google), tagged with the network, campaign and form. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


