# \WhatsAppApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_whats_app_group_participants**](WhatsAppApi.md#add_whats_app_group_participants) | **POST** /v1/whatsapp/wa-groups/{groupId}/participants | Add participants
[**approve_whats_app_group_join_requests**](WhatsAppApi.md#approve_whats_app_group_join_requests) | **POST** /v1/whatsapp/wa-groups/{groupId}/join-requests | Approve join requests
[**create_whats_app_group_chat**](WhatsAppApi.md#create_whats_app_group_chat) | **POST** /v1/whatsapp/wa-groups | Create group
[**create_whats_app_group_invite_link**](WhatsAppApi.md#create_whats_app_group_invite_link) | **POST** /v1/whatsapp/wa-groups/{groupId}/invite-link | Create invite link
[**create_whats_app_template**](WhatsAppApi.md#create_whats_app_template) | **POST** /v1/whatsapp/templates | Create template
[**delete_whats_app_group_chat**](WhatsAppApi.md#delete_whats_app_group_chat) | **DELETE** /v1/whatsapp/wa-groups/{groupId} | Delete group
[**delete_whats_app_template**](WhatsAppApi.md#delete_whats_app_template) | **DELETE** /v1/whatsapp/templates/{templateName} | Delete template
[**get_whats_app_business_profile**](WhatsAppApi.md#get_whats_app_business_profile) | **GET** /v1/whatsapp/business-profile | Get business profile
[**get_whats_app_display_name**](WhatsAppApi.md#get_whats_app_display_name) | **GET** /v1/whatsapp/business-profile/display-name | Get display name status
[**get_whats_app_group_chat**](WhatsAppApi.md#get_whats_app_group_chat) | **GET** /v1/whatsapp/wa-groups/{groupId} | Get group info
[**get_whats_app_template**](WhatsAppApi.md#get_whats_app_template) | **GET** /v1/whatsapp/templates/{templateName} | Get template
[**get_whats_app_templates**](WhatsAppApi.md#get_whats_app_templates) | **GET** /v1/whatsapp/templates | List templates
[**list_whats_app_group_chats**](WhatsAppApi.md#list_whats_app_group_chats) | **GET** /v1/whatsapp/wa-groups | List active groups
[**list_whats_app_group_join_requests**](WhatsAppApi.md#list_whats_app_group_join_requests) | **GET** /v1/whatsapp/wa-groups/{groupId}/join-requests | List join requests
[**reject_whats_app_group_join_requests**](WhatsAppApi.md#reject_whats_app_group_join_requests) | **DELETE** /v1/whatsapp/wa-groups/{groupId}/join-requests | Reject join requests
[**remove_whats_app_group_participants**](WhatsAppApi.md#remove_whats_app_group_participants) | **DELETE** /v1/whatsapp/wa-groups/{groupId}/participants | Remove participants
[**update_whats_app_business_profile**](WhatsAppApi.md#update_whats_app_business_profile) | **POST** /v1/whatsapp/business-profile | Update business profile
[**update_whats_app_display_name**](WhatsAppApi.md#update_whats_app_display_name) | **POST** /v1/whatsapp/business-profile/display-name | Request display name change
[**update_whats_app_group_chat**](WhatsAppApi.md#update_whats_app_group_chat) | **POST** /v1/whatsapp/wa-groups/{groupId} | Update group settings
[**update_whats_app_template**](WhatsAppApi.md#update_whats_app_template) | **PATCH** /v1/whatsapp/templates/{templateName} | Update template
[**upload_whats_app_profile_photo**](WhatsAppApi.md#upload_whats_app_profile_photo) | **POST** /v1/whatsapp/business-profile/photo | Upload profile picture



## add_whats_app_group_participants

> models::UnpublishPost200Response add_whats_app_group_participants(group_id, account_id, add_whats_app_group_participants_request)
Add participants

Add participants to a WhatsApp group. Maximum 8 participants per request. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**group_id** | **String** | Group ID | [required] |
**account_id** | **String** | WhatsApp social account ID | [required] |
**add_whats_app_group_participants_request** | [**AddWhatsAppGroupParticipantsRequest**](AddWhatsAppGroupParticipantsRequest.md) |  | [required] |

### Return type

[**models::UnpublishPost200Response**](unpublishPost_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## approve_whats_app_group_join_requests

> models::UnpublishPost200Response approve_whats_app_group_join_requests(group_id, account_id, approve_whats_app_group_join_requests_request)
Approve join requests

Approve pending join requests for a WhatsApp group. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**group_id** | **String** | Group ID | [required] |
**account_id** | **String** | WhatsApp social account ID | [required] |
**approve_whats_app_group_join_requests_request** | [**ApproveWhatsAppGroupJoinRequestsRequest**](ApproveWhatsAppGroupJoinRequestsRequest.md) |  | [required] |

### Return type

[**models::UnpublishPost200Response**](unpublishPost_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_whats_app_group_chat

> models::CreateWhatsAppGroupChat201Response create_whats_app_group_chat(create_whats_app_group_chat_request)
Create group

Create a new WhatsApp group chat. Returns the group ID and optionally an invite link. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_whats_app_group_chat_request** | [**CreateWhatsAppGroupChatRequest**](CreateWhatsAppGroupChatRequest.md) |  | [required] |

### Return type

[**models::CreateWhatsAppGroupChat201Response**](createWhatsAppGroupChat_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_whats_app_group_invite_link

> models::CreateWhatsAppGroupInviteLink200Response create_whats_app_group_invite_link(group_id, account_id)
Create invite link

Create a new invite link for a WhatsApp group. The previous link is revoked. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**group_id** | **String** | Group ID | [required] |
**account_id** | **String** | WhatsApp social account ID | [required] |

### Return type

[**models::CreateWhatsAppGroupInviteLink200Response**](createWhatsAppGroupInviteLink_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_whats_app_template

> models::CreateWhatsAppTemplate200Response create_whats_app_template(create_whats_app_template_request)
Create template

Create a new message template. Supports two modes:  **Custom template:** Provide `components` with your own content. Submitted to Meta for review (can take up to 24h).  **Library template:** Provide `library_template_name` instead of `components` to use a pre-built template from Meta's template library. Library templates are **pre-approved** (no review wait). You can optionally customize parameters and buttons via `library_template_body_inputs` and `library_template_button_inputs`.  Browse available library templates at: https://business.facebook.com/wa/manage/message-templates/ 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_whats_app_template_request** | [**CreateWhatsAppTemplateRequest**](CreateWhatsAppTemplateRequest.md) |  | [required] |

### Return type

[**models::CreateWhatsAppTemplate200Response**](createWhatsAppTemplate_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_whats_app_group_chat

> models::UnpublishPost200Response delete_whats_app_group_chat(group_id, account_id)
Delete group

Delete a WhatsApp group and remove all participants. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**group_id** | **String** | Group ID | [required] |
**account_id** | **String** | WhatsApp social account ID | [required] |

### Return type

[**models::UnpublishPost200Response**](unpublishPost_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_whats_app_template

> models::UnpublishPost200Response delete_whats_app_template(template_name, account_id)
Delete template

Permanently delete a message template by name. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**template_name** | **String** | Template name | [required] |
**account_id** | **String** | WhatsApp social account ID | [required] |

### Return type

[**models::UnpublishPost200Response**](unpublishPost_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_whats_app_business_profile

> models::GetWhatsAppBusinessProfile200Response get_whats_app_business_profile(account_id)
Get business profile

Retrieve the WhatsApp Business profile for the account (about, address, description, email, websites, etc.). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account ID | [required] |

### Return type

[**models::GetWhatsAppBusinessProfile200Response**](getWhatsAppBusinessProfile_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_whats_app_display_name

> models::GetWhatsAppDisplayName200Response get_whats_app_display_name(account_id)
Get display name status

Fetch the current display name and its Meta review status for a WhatsApp Business account. Display name changes require Meta approval and can take 1-3 business days. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account ID | [required] |

### Return type

[**models::GetWhatsAppDisplayName200Response**](getWhatsAppDisplayName_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_whats_app_group_chat

> models::GetWhatsAppGroupChat200Response get_whats_app_group_chat(group_id, account_id)
Get group info

Retrieve metadata about a WhatsApp group including subject, description, participants, and settings. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**group_id** | **String** | Group ID | [required] |
**account_id** | **String** | WhatsApp social account ID | [required] |

### Return type

[**models::GetWhatsAppGroupChat200Response**](getWhatsAppGroupChat_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_whats_app_template

> models::GetWhatsAppTemplate200Response get_whats_app_template(template_name, account_id)
Get template

Retrieve a single message template by name. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**template_name** | **String** | Template name | [required] |
**account_id** | **String** | WhatsApp social account ID | [required] |

### Return type

[**models::GetWhatsAppTemplate200Response**](getWhatsAppTemplate_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_whats_app_templates

> models::GetWhatsAppTemplates200Response get_whats_app_templates(account_id)
List templates

List all message templates for the WhatsApp Business Account (WABA) associated with the given account. Templates are fetched directly from the WhatsApp Cloud API. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account ID | [required] |

### Return type

[**models::GetWhatsAppTemplates200Response**](getWhatsAppTemplates_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_whats_app_group_chats

> models::ListWhatsAppGroupChats200Response list_whats_app_group_chats(account_id, limit, after)
List active groups

List active WhatsApp group chats for a business phone number. These are actual WhatsApp group conversations on the platform. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account ID | [required] |
**limit** | Option<**i32**> | Max groups to return |  |[default to 25]
**after** | Option<**String**> | Pagination cursor |  |

### Return type

[**models::ListWhatsAppGroupChats200Response**](listWhatsAppGroupChats_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_whats_app_group_join_requests

> models::ListWhatsAppGroupJoinRequests200Response list_whats_app_group_join_requests(group_id, account_id)
List join requests

List pending join requests for a WhatsApp group (only for groups with approval_required mode). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**group_id** | **String** | Group ID | [required] |
**account_id** | **String** | WhatsApp social account ID | [required] |

### Return type

[**models::ListWhatsAppGroupJoinRequests200Response**](listWhatsAppGroupJoinRequests_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reject_whats_app_group_join_requests

> models::UnpublishPost200Response reject_whats_app_group_join_requests(group_id, account_id, reject_whats_app_group_join_requests_request)
Reject join requests

Reject pending join requests for a WhatsApp group. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**group_id** | **String** | Group ID | [required] |
**account_id** | **String** | WhatsApp social account ID | [required] |
**reject_whats_app_group_join_requests_request** | [**RejectWhatsAppGroupJoinRequestsRequest**](RejectWhatsAppGroupJoinRequestsRequest.md) |  | [required] |

### Return type

[**models::UnpublishPost200Response**](unpublishPost_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_whats_app_group_participants

> models::UnpublishPost200Response remove_whats_app_group_participants(group_id, account_id, remove_whats_app_group_participants_request)
Remove participants

Remove participants from a WhatsApp group. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**group_id** | **String** | Group ID | [required] |
**account_id** | **String** | WhatsApp social account ID | [required] |
**remove_whats_app_group_participants_request** | [**RemoveWhatsAppGroupParticipantsRequest**](RemoveWhatsAppGroupParticipantsRequest.md) |  | [required] |

### Return type

[**models::UnpublishPost200Response**](unpublishPost_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_whats_app_business_profile

> models::UnpublishPost200Response update_whats_app_business_profile(update_whats_app_business_profile_request)
Update business profile

Update the WhatsApp Business profile. All fields are optional; only provided fields will be updated. Constraints: about max 139 chars, description max 512 chars, max 2 websites. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**update_whats_app_business_profile_request** | [**UpdateWhatsAppBusinessProfileRequest**](UpdateWhatsAppBusinessProfileRequest.md) |  | [required] |

### Return type

[**models::UnpublishPost200Response**](unpublishPost_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_whats_app_display_name

> models::UpdateWhatsAppDisplayName200Response update_whats_app_display_name(update_whats_app_display_name_request)
Request display name change

Submit a display name change request for the WhatsApp Business account. The new name must follow WhatsApp naming guidelines (3-512 characters, must represent your business). Changes require Meta review and approval, which typically takes 1-3 business days. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**update_whats_app_display_name_request** | [**UpdateWhatsAppDisplayNameRequest**](UpdateWhatsAppDisplayNameRequest.md) |  | [required] |

### Return type

[**models::UpdateWhatsAppDisplayName200Response**](updateWhatsAppDisplayName_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_whats_app_group_chat

> models::UnpublishPost200Response update_whats_app_group_chat(group_id, account_id, update_whats_app_group_chat_request)
Update group settings

Update the subject, description, or join approval mode of a WhatsApp group. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**group_id** | **String** | Group ID | [required] |
**account_id** | **String** | WhatsApp social account ID | [required] |
**update_whats_app_group_chat_request** | [**UpdateWhatsAppGroupChatRequest**](UpdateWhatsAppGroupChatRequest.md) |  | [required] |

### Return type

[**models::UnpublishPost200Response**](unpublishPost_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_whats_app_template

> models::UpdateWhatsAppTemplate200Response update_whats_app_template(template_name, update_whats_app_template_request)
Update template

Update a message template's components. Only certain fields can be updated depending on the template's current approval state. Approved templates can only have components updated. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**template_name** | **String** | Template name | [required] |
**update_whats_app_template_request** | [**UpdateWhatsAppTemplateRequest**](UpdateWhatsAppTemplateRequest.md) |  | [required] |

### Return type

[**models::UpdateWhatsAppTemplate200Response**](updateWhatsAppTemplate_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## upload_whats_app_profile_photo

> models::UnpublishPost200Response upload_whats_app_profile_photo(account_id, file)
Upload profile picture

Upload a new profile picture for the WhatsApp Business Profile. Uses Meta's resumable upload API under the hood: creates an upload session, uploads the image bytes, then updates the business profile with the resulting handle. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account ID | [required] |
**file** | **std::path::PathBuf** | Image file (JPEG or PNG, max 5MB, recommended 640x640) | [required] |

### Return type

[**models::UnpublishPost200Response**](unpublishPost_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

