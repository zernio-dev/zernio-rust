# \LeadFormsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_lead_form**](LeadFormsApi.md#create_lead_form) | **POST** /v1/ads/lead-forms | Create a Meta Lead Gen Form
[**create_lead_form_test_lead**](LeadFormsApi.md#create_lead_form_test_lead) | **POST** /v1/ads/lead-forms/{formId}/test-leads | Create a synthetic test lead
[**delete_lead_form**](LeadFormsApi.md#delete_lead_form) | **DELETE** /v1/ads/lead-forms/{formId} | Delete a Lead Gen Form
[**delete_lead_form_test_lead**](LeadFormsApi.md#delete_lead_form_test_lead) | **DELETE** /v1/ads/lead-forms/{formId}/test-leads/{leadId} | Delete a (test) lead
[**get_lead_form**](LeadFormsApi.md#get_lead_form) | **GET** /v1/ads/lead-forms/{formId} | Get a Lead Gen Form
[**list_lead_form_leads**](LeadFormsApi.md#list_lead_form_leads) | **GET** /v1/ads/lead-forms/{formId}/leads | List submitted leads for a form
[**list_lead_forms**](LeadFormsApi.md#list_lead_forms) | **GET** /v1/ads/lead-forms | List Meta Lead Gen Forms
[**update_lead_form**](LeadFormsApi.md#update_lead_form) | **PATCH** /v1/ads/lead-forms/{formId} | Update a Lead Gen Form (status only)



## create_lead_form

> models::CreateLeadForm201Response create_lead_form(create_lead_form_body)
Create a Meta Lead Gen Form

Creates a new Instant Form on the Facebook Page tied to the given social account. The form is created in `ACTIVE` status and is immediately attachable to ads (see `leadGenFormId` on POST /v1/ads/create).  Once a form has received any leads, its questions / privacy policy / thank-you page become immutable on Meta's side; only `status` may be changed via PATCH. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_lead_form_body** | [**CreateLeadFormBody**](CreateLeadFormBody.md) |  | [required] |

### Return type

[**models::CreateLeadForm201Response**](createLeadForm_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_lead_form_test_lead

> models::CreateLeadFormTestLead200Response create_lead_form_test_lead(form_id, create_lead_form_test_lead_request)
Create a synthetic test lead

Submits a fake lead against a form. Useful for QA, App Review demos, and exercising webhook subscribers without waiting for real ad impressions. Meta caps a form to one outstanding test lead — call DELETE on the returned id before re-submitting. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**form_id** | **String** |  | [required] |
**create_lead_form_test_lead_request** | [**CreateLeadFormTestLeadRequest**](CreateLeadFormTestLeadRequest.md) |  | [required] |

### Return type

[**models::CreateLeadFormTestLead200Response**](createLeadFormTestLead_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_lead_form

> models::DeleteLeadForm200Response delete_lead_form(form_id, account_id)
Delete a Lead Gen Form

Deletes the form from Meta. If the form has already received leads, Meta archives it instead of hard-deleting; the response is the same either way. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**form_id** | **String** |  | [required] |
**account_id** | **String** |  | [required] |

### Return type

[**models::DeleteLeadForm200Response**](deleteLeadForm_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_lead_form_test_lead

> models::DeleteLeadForm200Response delete_lead_form_test_lead(form_id, lead_id, account_id)
Delete a (test) lead

Deletes a single lead by ID. Primarily used to clear the outstanding test lead so you can submit a new one. The same Graph API call works on real leads too; for production lead deletion (GDPR/CCPA) prefer a dedicated flow. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**form_id** | **String** |  | [required] |
**lead_id** | **String** |  | [required] |
**account_id** | **String** |  | [required] |

### Return type

[**models::DeleteLeadForm200Response**](deleteLeadForm_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_lead_form

> models::GetLeadForm200Response get_lead_form(form_id, account_id)
Get a Lead Gen Form

Returns full details for a single form, including questions, privacy policy, and lead counts.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**form_id** | **String** | Meta lead form ID (numeric string) | [required] |
**account_id** | **String** |  | [required] |

### Return type

[**models::GetLeadForm200Response**](getLeadForm_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_lead_form_leads

> models::ListLeadFormLeads200Response list_lead_form_leads(form_id, account_id, limit, cursor, since)
List submitted leads for a form

Returns leads submitted against a Lead Gen Form. The page access token on the connected account must have the `leads_retrieval` permission — if the token was minted before that scope was approved, this endpoint returns `code: scope_reconnect_required` (HTTP 422) and the customer must reconnect the Facebook account.  For real-time delivery without polling, subscribe a webhook to the `lead.received` event. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**form_id** | **String** |  | [required] |
**account_id** | **String** |  | [required] |
**limit** | Option<**i32**> |  |  |[default to 25]
**cursor** | Option<**String**> |  |  |
**since** | Option<**i32**> | Unix timestamp; only return leads created strictly after this. |  |

### Return type

[**models::ListLeadFormLeads200Response**](listLeadFormLeads_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_lead_forms

> models::ListLeadForms200Response list_lead_forms(account_id, limit, cursor)
List Meta Lead Gen Forms

Returns Meta Instant Forms attached to the Facebook Page connected via the given social account. Forms live on Facebook Pages — Instagram lead ads reuse the linked Page under the hood, so even Instagram-only ad accounts list forms from the linked Facebook Page. Requires the Ads add-on. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Facebook social account ID (Late SocialAccount _id) | [required] |
**limit** | Option<**i32**> |  |  |[default to 25]
**cursor** | Option<**String**> | Meta `paging.cursors.after` from a prior page |  |

### Return type

[**models::ListLeadForms200Response**](listLeadForms_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_lead_form

> models::DeleteLeadForm200Response update_lead_form(form_id, update_lead_form_request)
Update a Lead Gen Form (status only)

Update mutable fields on an existing form. Today only `status` is mutable on Meta's side — questions / privacy_policy / thank_you_page are immutable once a form has received any leads. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**form_id** | **String** |  | [required] |
**update_lead_form_request** | [**UpdateLeadFormRequest**](UpdateLeadFormRequest.md) |  | [required] |

### Return type

[**models::DeleteLeadForm200Response**](deleteLeadForm_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

