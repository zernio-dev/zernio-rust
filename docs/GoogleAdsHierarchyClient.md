# GoogleAdsHierarchyClient

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**customer_id** | Option<**String**> | Native Google Ads customer id, digits only. | [optional]
**name** | Option<**String**> | Null for a pending invitation. | [optional]
**currency** | Option<**String**> |  | [optional]
**time_zone** | Option<**String**> |  | [optional]
**manager** | Option<**bool**> | True for a sub-manager account. | [optional]
**test_account** | Option<**bool**> |  | [optional]
**hidden** | Option<**bool**> | Hidden in the manager's Google Ads UI. | [optional]
**level** | Option<**i32**> | Distance from the root (1 = direct client of the root). | [optional]
**status** | Option<**String**> | Google customer status: ENABLED, CANCELED, SUSPENDED or CLOSED. Null for a pending invitation. | [optional]
**parent_customer_id** | Option<**String**> | Direct manager of this account. Null only when more than 50 managers under the root were skipped. | [optional]
**manager_link_id** | Option<**String**> | Id of the link to the parent, used by PATCH /v1/ads/accounts/manager-links. | [optional]
**link_status** | Option<**LinkStatus**> |  (enum: ACTIVE, PENDING, ) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


