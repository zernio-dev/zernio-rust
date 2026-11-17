# UpdateHubSpotSettingsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sync_contacts** | Option<**bool**> | Create a HubSpot contact for an inbox contact that matches none by email or phone. A match is linked as it is and never updated. | [optional]
**log_messages** | Option<**bool**> | Log inbound and outbound inbox messages on the contact's HubSpot timeline. | [optional]
**log_delivery_status** | Option<**bool**> | Add the delivery status of each outgoing WhatsApp, SMS or RCS message to its timeline entry and update it as the message is delivered, read or fails. A failure shows the reason and its code. Only applies while `logMessages` is on. | [optional]
**contact_defaults** | Option<**std::collections::HashMap<String, String>**> | Values for contact properties your portal requires on create, keyed by HubSpot internal name (lowercase letters, digits, underscores), for example `{\"lifecyclestage\": \"lead\"}`. Replaces the whole map; send `{}` to clear it. Clears `syncIssue` until the next contact create tells whether the portal accepts them. | [optional]
**report_deals** | Option<**bool**> | Send each deal that becomes closed won as a Purchase to the profile's event destinations, about once an hour. Requires the portal to have granted `crm.objects.deals.read`; otherwise 400. Deals closed before it was turned on are not sent. | [optional]
**use_deals_as_results** | Option<**bool**> | Count each closed-won deal as a sale with its amount on the ad campaign that brought its contact, in `GET /v1/ads/campaign-results` and ad rules. Requires `crm.objects.deals.read`; otherwise 400. Turning it on fills in the deals of the last 90 days, never sent to the ad platforms. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


