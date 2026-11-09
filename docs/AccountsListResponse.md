# AccountsListResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**accounts** | [**Vec<models::ListedAccount>**](ListedAccount.md) |  | 
**has_analytics_access** | **bool** | Whether user has analytics add-on access | 
**pagination** | Option<[**models::AccountsListResponsePagination**](AccountsListResponsePagination.md)> |  | [optional]
**warning** | Option<**String**> | Only when an unpaged API request was cut at 500 accounts: how to list the rest with cursor paging. | [optional]
**profile_totals** | Option<**std::collections::HashMap<String, i32>**> | Only with profileIds and perProfile. Accounts matching the filters per profile ID; a profile with none is absent. | [optional]
**status_counts** | Option<[**models::AccountsListResponseStatusCounts**](AccountsListResponseStatusCounts.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


