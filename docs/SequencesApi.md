# \SequencesApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**activate_sequence**](SequencesApi.md#activate_sequence) | **POST** /v1/sequences/{sequenceId}/activate | Activate sequence
[**create_sequence**](SequencesApi.md#create_sequence) | **POST** /v1/sequences | Create sequence
[**delete_sequence**](SequencesApi.md#delete_sequence) | **DELETE** /v1/sequences/{sequenceId} | Delete sequence
[**enroll_contacts**](SequencesApi.md#enroll_contacts) | **POST** /v1/sequences/{sequenceId}/enroll | Enroll contacts in a sequence
[**get_sequence**](SequencesApi.md#get_sequence) | **GET** /v1/sequences/{sequenceId} | Get sequence with steps
[**list_sequence_enrollments**](SequencesApi.md#list_sequence_enrollments) | **GET** /v1/sequences/{sequenceId}/enrollments | List enrollments for a sequence
[**list_sequences**](SequencesApi.md#list_sequences) | **GET** /v1/sequences | List sequences
[**pause_sequence**](SequencesApi.md#pause_sequence) | **POST** /v1/sequences/{sequenceId}/pause | Pause sequence
[**unenroll_contact**](SequencesApi.md#unenroll_contact) | **DELETE** /v1/sequences/{sequenceId}/enroll/{contactId} | Unenroll contact
[**update_sequence**](SequencesApi.md#update_sequence) | **PATCH** /v1/sequences/{sequenceId} | Update sequence



## activate_sequence

> models::ActivateSequence200Response activate_sequence(sequence_id)
Activate sequence

Start a draft or paused sequence. The sequence must have at least one step.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sequence_id** | **String** |  | [required] |

### Return type

[**models::ActivateSequence200Response**](activateSequence_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_sequence

> models::CreateSequence200Response create_sequence(create_sequence_request)
Create sequence

Create a multi-step messaging sequence. Each step has a delay and a message or WhatsApp template.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_sequence_request** | [**CreateSequenceRequest**](CreateSequenceRequest.md) |  | [required] |

### Return type

[**models::CreateSequence200Response**](createSequence_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_sequence

> delete_sequence(sequence_id)
Delete sequence

Permanently delete a sequence. Active enrollments are stopped.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sequence_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## enroll_contacts

> models::EnrollContacts200Response enroll_contacts(sequence_id, enroll_contacts_request)
Enroll contacts in a sequence

Enroll one or more contacts into a sequence. Contacts already enrolled are skipped.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sequence_id** | **String** |  | [required] |
**enroll_contacts_request** | [**EnrollContactsRequest**](EnrollContactsRequest.md) |  | [required] |

### Return type

[**models::EnrollContacts200Response**](enrollContacts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_sequence

> models::GetSequence200Response get_sequence(sequence_id)
Get sequence with steps

Returns a sequence with all its steps and enrollment stats.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sequence_id** | **String** |  | [required] |

### Return type

[**models::GetSequence200Response**](getSequence_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_sequence_enrollments

> models::ListSequenceEnrollments200Response list_sequence_enrollments(sequence_id, status, limit, skip)
List enrollments for a sequence

Returns enrolled contacts with their progress, status, and next scheduled step.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sequence_id** | **String** |  | [required] |
**status** | Option<**String**> |  |  |
**limit** | Option<**i32**> |  |  |[default to 50]
**skip** | Option<**i32**> |  |  |[default to 0]

### Return type

[**models::ListSequenceEnrollments200Response**](listSequenceEnrollments_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_sequences

> models::ListSequences200Response list_sequences(profile_id, status, limit, skip)
List sequences

Returns sequences with enrollment stats. Filter by status, platform, or profile.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | Option<**String**> | Filter by profile. Omit to list across all profiles |  |
**status** | Option<**String**> |  |  |
**limit** | Option<**i32**> |  |  |[default to 50]
**skip** | Option<**i32**> |  |  |[default to 0]

### Return type

[**models::ListSequences200Response**](listSequences_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## pause_sequence

> models::ActivateSequence200Response pause_sequence(sequence_id)
Pause sequence

Pause an active sequence. Enrolled contacts stop receiving messages until the sequence is reactivated.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sequence_id** | **String** |  | [required] |

### Return type

[**models::ActivateSequence200Response**](activateSequence_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## unenroll_contact

> unenroll_contact(sequence_id, contact_id)
Unenroll contact

Remove a contact from a sequence. No further messages will be sent to this contact.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sequence_id** | **String** |  | [required] |
**contact_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_sequence

> models::UpdateSequence200Response update_sequence(sequence_id)
Update sequence

Update a sequence's name, steps, or exit conditions. Active sequences can be updated without pausing.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sequence_id** | **String** |  | [required] |

### Return type

[**models::UpdateSequence200Response**](updateSequence_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

