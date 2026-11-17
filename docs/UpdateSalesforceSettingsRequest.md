# UpdateSalesforceSettingsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sync_contacts** | Option<**bool**> | Create a Lead or Contact for an inbox contact that matches nobody by phone (any phone field) or email. A match is linked as it is and never updated. | [optional]
**log_messages** | Option<**bool**> | Log inbound and outbound inbox messages as one conversation Task per person, channel and day. | [optional]
**create_as** | Option<**CreateAs**> | What a person new to Salesforce is created as. Leads get Company `[not provided]`. (enum: lead, contact) | [optional]
**log_delivery_status** | Option<**bool**> | Mark sent messages in the transcript as delivered, read or failed. | [optional]
**use_opportunities_in_results** | Option<**bool**> | Count closed-won Opportunities as sales on the ad campaign named by their Primary Campaign Source, in campaign results and ad rules. Turning it on also fills in the Opportunities won in the last 90 days. Lost or reopened Opportunities stop counting. | [optional]
**report_opportunities_to_ads** | Option<**bool**> | Send each newly closed-won Opportunity once as a Purchase event (source `salesforce`, event id `salesforce_opp_{orgId}_{opportunityId}`) to the profile's event destinations, with the email and phone of its primary contact role, else the first Contact of its Account. Opportunities won before it was turned on are not sent. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


