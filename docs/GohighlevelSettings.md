# GohighlevelSettings

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | **String** |  | 
**platform** | **Platform** |  (enum: gohighlevel) | 
**location_id** | **String** | The HighLevel sub-account (location) id. | 
**company_id** | Option<**String**> | The agency that owns the sub-account, null for a sub-account under no agency. | 
**location_name** | Option<**String**> |  | 
**installed_by** | Option<**String**> | The HighLevel user who installed the app. | 
**relay_conversions** | **bool** | CRM events are relayed as conversions. Default true. | 
**write_back_attribution** | **bool** | Relayed conversions are written back onto the HighLevel contact. Default true. | 
**report_to_ads** | **bool** | Relayed conversions are forwarded to the profile's ad platforms. A new connection starts with this on when its profile already sends events to an ad account, else off; reconnecting keeps the value. | 
**sync_contacts** | **bool** | Inbox contacts are matched to HighLevel contacts by phone, then email, and created there when none matches. Default true. | 
**log_messages** | **bool** | Inbox messages from every channel (both directions) are logged on the HighLevel contact as one note per channel and day. Default true. | 
**log_delivery_status** | **bool** | Logged outgoing messages show their delivery status (sent, delivered, read, failed) on their note line. Default true. | 
**sync_ad_leads** | **bool** | Leads from the profile's ad network lead forms become HighLevel contacts, deduplicated by email, then phone. Default true. | 
**mirror_conversations** | **bool** | Telegram, LINE, WeChat, iMessage and RCS messages go into the contact's Conversations thread under the Zernio channel (answerable from HighLevel) instead of a note. Default true. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


