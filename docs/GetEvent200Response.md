# GetEvent200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**event** | Option<[**models::StoredEvent**](StoredEvent.md)> |  | [optional]
**deliveries** | Option<[**Vec<models::GetEvent200ResponseDeliveriesInner>**](GetEvent200ResponseDeliveriesInner.md)> |  | [optional]
**touches** | Option<[**Vec<models::GetEvent200ResponseTouchesInner>**](GetEvent200ResponseTouchesInner.md)> | The touches of the person before the event that its credit is split across, oldest first: website visits from somewhere (an ad click, search, a tagged link) and earlier lead forms or sales. Empty when the event counts whole for its own campaign under every model. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


