# GetEvent200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**event** | Option<[**models::StoredEvent**](StoredEvent.md)> |  | [optional]
**deliveries** | Option<[**Vec<models::GetEvent200ResponseDeliveriesInner>**](GetEvent200ResponseDeliveriesInner.md)> |  | [optional]
**touches** | Option<[**Vec<models::GetEvent200ResponseTouchesInner>**](GetEvent200ResponseTouchesInner.md)> | The touches the event is split across, oldest first: website visits (an ad click, search, a tagged link), the first and latest visits HubSpot recorded for a deal, earlier lead forms or sales, and a Shopify buyer's post-purchase survey answer. Empty when the event counts whole for its own campaign. | [optional]
**after** | Option<[**Vec<models::GetEvent200ResponseAfterInner>**](GetEvent200ResponseAfterInner.md)> | The same person's events in the 180 days after this one, oldest first, up to 50, like a Stripe payment after a sign-up. People match on email, phone, external id or visitor id. Copies of this event, and website copies of a sale a server reported, are left out. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


