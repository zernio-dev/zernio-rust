# AccountsListResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**accounts** | [**Vec<models::SocialAccount>**](SocialAccount.md) |  | 
**has_analytics_access** | **bool** | Whether user has analytics add-on access | 
**pagination** | Option<[**models::Pagination**](Pagination.md)> | Only present when page/limit params are provided | [optional]
**profile_totals** | Option<**std::collections::HashMap<String, i32>**> | Only with profileIds and perProfile. Accounts matching the filters per profile ID; a profile with none is absent. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


