# GetAdAccountHierarchy200ResponseRootsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**customer_id** | Option<**String**> | Native Google Ads customer id, digits only. | [optional]
**name** | Option<**String**> |  | [optional]
**currency** | Option<**String**> | ISO 4217 code. | [optional]
**time_zone** | Option<**String**> | IANA time zone, e.g. Europe/Madrid. | [optional]
**manager** | Option<**bool**> | True for a manager (MCC) account. | [optional]
**test_account** | Option<**bool**> |  | [optional]
**status** | Option<**String**> | Google customer status: ENABLED, CANCELED, SUSPENDED or CLOSED. | [optional]
**manager_links** | Option<[**Vec<models::GetAdAccountHierarchy200ResponseRootsInnerManagerLinksInner>**](GetAdAccountHierarchy200ResponseRootsInnerManagerLinksInner.md)> | Managers linked to this account, ACTIVE or PENDING. | [optional]
**clients** | Option<[**Vec<models::GoogleAdsHierarchyClient>**](GoogleAdsHierarchyClient.md)> | Every account under this root at any depth, in Google's order, followed by pending invitations. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


