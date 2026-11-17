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
**log_delivery_status** | **bool** | Whether sent messages in the transcript are marked delivered, read or failed. | 
**sync_issue** | [**models::SalesforceSettingsSyncIssue**](SalesforceSettingsSyncIssue.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


