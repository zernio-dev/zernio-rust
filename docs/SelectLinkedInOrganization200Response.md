# SelectLinkedInOrganization200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | Option<**String**> |  | [optional]
**redirect_url** | Option<**String**> | The redirect URL with connection params appended (only if redirect_url was provided in request) | [optional]
**account** | Option<[**models::SelectLinkedInOrganization200ResponseAccount**](SelectLinkedInOrganization200ResponseAccount.md)> |  | [optional]
**accounts** | Option<**Vec<serde_json::Value>**> | selections only. The connected accounts, same shape as `account`. The redirect_url then carries `accountIds` (comma-separated) and `accountId` of the first. | [optional]
**failed** | Option<[**Vec<models::SelectLinkedInOrganization200ResponseFailedInner>**](SelectLinkedInOrganization200ResponseFailedInner.md)> | selections only. The accounts that could not be connected while the others were. `id` is the organization URN or the member id, or `selections[i]` for an entry naming neither. | [optional]
**bulk_refresh** | Option<[**models::SelectLinkedInOrganization200ResponseBulkRefresh**](SelectLinkedInOrganization200ResponseBulkRefresh.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


