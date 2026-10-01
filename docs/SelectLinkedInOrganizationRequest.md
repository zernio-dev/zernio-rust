# SelectLinkedInOrganizationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** |  | 
**temp_token** | **String** |  | 
**user_profile** | **serde_json::Value** |  | 
**account_type** | Option<**AccountType**> | Send this (with selectedOrganization for an organization) or selections, not both. (enum: personal, organization) | [optional]
**selections** | Option<[**Vec<models::SelectLinkedInOrganizationRequestSelectionsInner>**](SelectLinkedInOrganizationRequestSelectionsInner.md)> | Several accounts to connect from one sign-in (yourself and/or organizations), each as its own account. With two or more entries the response lists `accounts` and `failed` instead of `account`, and the request is refused with 400 on a reconnect or an ads connect. A single entry behaves exactly like accountType. | [optional]
**selected_organization** | Option<[**models::SelectLinkedInOrganizationRequestSelectedOrganization**](SelectLinkedInOrganizationRequestSelectedOrganization.md)> |  | [optional]
**redirect_url** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


