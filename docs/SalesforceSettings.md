# SalesforceSettings

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | **String** | Zernio account ID of the Salesforce connection. | 
**platform** | **Platform** |  (enum: salesforce) | 
**org_id** | **String** | 18-character Salesforce organization ID. | 
**org_name** | Option<**String**> | The org's name, when the connected user can read it. | 
**environment** | **Environment** | Whether the org was connected through login.salesforce.com or test.salesforce.com. (enum: production, sandbox) | 
**instance_url** | **String** | The org's API host, for example `https://acme.my.salesforce.com`. | 
**installed_by** | Option<**String**> | Email or username of the Salesforce user who connected the org. | 
**sync_contacts** | **bool** | Whether Zernio creates a Lead or Contact (per `createAs`) for an inbox contact that matches nobody by phone or email. | 
**log_messages** | **bool** | Whether Zernio logs inbox messages. Each person, channel and UTC day gets one completed Task (subject `WhatsApp conversation · 2026-11-17`) whose Description holds the transcript; a day past 32,000 characters continues in a Task marked \"(part 2)\". | 
**create_as** | **CreateAs** | What a person new to Salesforce is created as. (enum: lead, contact) | 
**log_delivery_status** | **bool** | Whether sent WhatsApp, SMS and RCS messages in the transcript are marked sent, delivered, read, played or failed. | 
**sync_issue** | [**models::SalesforceSettingsSyncIssue**](SalesforceSettingsSyncIssue.md) |  | 
**use_opportunities_in_results** | **bool** | Whether closed-won Opportunities count as sales (Amount, in the Opportunity's or the org's currency) on the ad campaign named by their Primary Campaign Source, in campaign results and ad rules. Lost or reopened Opportunities stop counting. | 
**report_opportunities_to_ads** | **bool** | Whether Zernio sends newly closed-won Opportunities as Purchase events (source `salesforce`) to the profile's event destinations. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


