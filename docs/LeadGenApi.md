# \LeadGenApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**archive_lead_form**](LeadGenApi.md#archive_lead_form) | **DELETE** /v1/ads/lead-forms/{formId} | Archive a lead form
[**create_lead_form**](LeadGenApi.md#create_lead_form) | **POST** /v1/ads/lead-forms | Create a lead form
[**create_test_lead**](LeadGenApi.md#create_test_lead) | **POST** /v1/ads/lead-forms/{formId}/test-leads | Create a test lead
[**get_lead_form**](LeadGenApi.md#get_lead_form) | **GET** /v1/ads/lead-forms/{formId} | Get a lead form
[**list_form_leads**](LeadGenApi.md#list_form_leads) | **GET** /v1/ads/lead-forms/{formId}/leads | List leads for a single form
[**list_lead_forms**](LeadGenApi.md#list_lead_forms) | **GET** /v1/ads/lead-forms | List lead forms
[**list_leads**](LeadGenApi.md#list_leads) | **GET** /v1/ads/leads | List submitted leads



## archive_lead_form

> models::ArchiveLeadForm200Response archive_lead_form(form_id, account_id)
Archive a lead form

Neither platform hard-deletes a form; this archives it (Meta status=ARCHIVED; LinkedIn state=ARCHIVED via PARTIAL_UPDATE).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**form_id** | **String** | Numeric form id (Meta leadgen_form id or LinkedIn leadForm id). | [required] |
**account_id** | **String** | Connected facebook or linkedin ads account id (selects the platform). | [required] |

### Return type

[**models::ArchiveLeadForm200Response**](archiveLeadForm_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_lead_form

> models::CreateLeadForm200Response create_lead_form(create_lead_form_request)
Create a lead form

Creates a Lead Gen form. The form content goes inside `platformSpecificData` for both platforms (the shape is selected by the accountId's platform). Meta: created on the connected Facebook Page (POST /{page-id}/leadgen_forms); the old top-level Meta fields (questions, thankYou*, contextCard, …) are DEPRECATED but still accepted while platformSpecificData is absent — mixing both shapes is a 400. LinkedIn: created on the ad account's Company Page. NOT idempotent — a retry creates a second form. Meta prefilled question types (EMAIL, PHONE, FULL_NAME, …) must omit label/key; CUSTOM questions require both. LinkedIn exposes only free-text and multiple-choice questions via API (prefilled-from-profile fields are Campaign Manager UI-only). Requires the Ads add-on. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_lead_form_request** | [**CreateLeadFormRequest**](CreateLeadFormRequest.md) |  | [required] |

### Return type

[**models::CreateLeadForm200Response**](createLeadForm_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_test_lead

> models::CreateTestLead200Response create_test_lead(form_id, create_test_lead_request)
Create a test lead

Submits a test lead against the form (POST /{form-id}/test_leads) to exercise retrieval without waiting for real ad impressions. Meta allows one test lead per form at a time. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**form_id** | **String** |  | [required] |
**create_test_lead_request** | [**CreateTestLeadRequest**](CreateTestLeadRequest.md) |  | [required] |

### Return type

[**models::CreateTestLead200Response**](createTestLead_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_lead_form

> models::GetLeadForm200Response get_lead_form(form_id, account_id)
Get a lead form

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**form_id** | **String** | Numeric form id (Meta leadgen_form id or LinkedIn leadForm id). | [required] |
**account_id** | **String** | Connected facebook or linkedin ads account id (selects the platform). | [required] |

### Return type

[**models::GetLeadForm200Response**](getLeadForm_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_form_leads

> models::ListFormLeads200Response list_form_leads(form_id, account_id, limit, cursor, since)
List leads for a single form

Returns leads for one form. Serves persisted leads (ingested via the leadgen webhook) when available, falling back to a live Graph read. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**form_id** | **String** |  | [required] |
**account_id** | **String** |  | [required] |
**limit** | Option<**i32**> |  |  |[default to 25]
**cursor** | Option<**String**> |  |  |
**since** | Option<**i32**> | Unix seconds. |  |

### Return type

[**models::ListFormLeads200Response**](listFormLeads_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_lead_forms

> models::ListLeadForms200Response list_lead_forms(account_id, ad_account_id, limit, cursor)
List lead forms

Lists the Lead Gen forms owned by the account. Meta: forms on the connected Facebook Page. LinkedIn: forms owned by the ad account's Company Page — pass `adAccountId` (LinkedIn forms are org-owned). Requires the Ads add-on. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected facebook or linkedin ads account id. | [required] |
**ad_account_id** | Option<**String**> | LinkedIn only: the LinkedIn ad account id (used to resolve the owning organization). Required for LinkedIn. |  |
**limit** | Option<**i32**> |  |  |[default to 25]
**cursor** | Option<**String**> |  |  |

### Return type

[**models::ListLeadForms200Response**](listLeadForms_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_leads

> models::ListLeads200Response list_leads(form_id, account_id, ad_account_id, limit, since, cursor)
List submitted leads

Returns submitted Lead Gen leads for your team, newest-first, with keyset pagination on `cursor`. For Meta (default) leads are served from the persisted cache, ingested in real time from the `leadgen` webhook. When `accountId` is a LinkedIn ads account, leads are fetched live from LinkedIn's `leadFormResponses` (LinkedIn has no webhook and enforces 90-day retention, so nothing is persisted) and `adAccountId` is required. Reading LinkedIn responses needs the `r_marketing_leadgen_automation` permission; accounts connected before it was added must reconnect. Requires the Ads add-on. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**form_id** | Option<**String**> | Filter to a single lead form. |  |
**account_id** | Option<**String**> | Filter to a single connected account. LinkedIn ads accounts switch to the live fetch. |  |
**ad_account_id** | Option<**String**> | LinkedIn only: the LinkedIn ad account id whose responses to read (owner-scoped finder). |  |
**limit** | Option<**i32**> |  |  |[default to 25]
**since** | Option<**i32**> | Unix seconds; only leads created at/after this timestamp. |  |
**cursor** | Option<**String**> | Keyset cursor from a previous response's pagination.cursor (Meta: AdLead id; LinkedIn: numeric start offset). |  |

### Return type

[**models::ListLeads200Response**](listLeads_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

