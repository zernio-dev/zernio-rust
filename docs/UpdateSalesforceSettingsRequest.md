# UpdateSalesforceSettingsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sync_contacts** | Option<**bool**> | Create a Lead or Contact for an inbox contact that matches nobody by phone (any phone field) or email. A match is linked as it is and never updated. | [optional]
**log_messages** | Option<**bool**> | Log inbound and outbound inbox messages as one conversation Task per person, channel and day. | [optional]
**create_as** | Option<**CreateAs**> | What a person new to Salesforce is created as. Leads get Company `[not provided]`. (enum: lead, contact) | [optional]
**log_delivery_status** | Option<**bool**> | Mark sent messages in the transcript as delivered, read or failed. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


