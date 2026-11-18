# \CrmApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_crm_activity**](CrmApi.md#create_crm_activity) | **POST** /v1/crm/{accountId}/contacts/{contactId}/activities | Log a CRM activity
[**create_crm_contact**](CrmApi.md#create_crm_contact) | **POST** /v1/crm/{accountId}/contacts | Create a CRM contact
[**get_crm_contact**](CrmApi.md#get_crm_contact) | **GET** /v1/crm/{accountId}/contacts/{contactId} | Get a CRM contact
[**get_crm_deal**](CrmApi.md#get_crm_deal) | **GET** /v1/crm/{accountId}/deals/{dealId} | Get a CRM deal
[**list_crm_deals**](CrmApi.md#list_crm_deals) | **GET** /v1/crm/{accountId}/deals | List CRM deals
[**list_crm_owners**](CrmApi.md#list_crm_owners) | **GET** /v1/crm/{accountId}/owners | List CRM owners
[**search_crm_contacts**](CrmApi.md#search_crm_contacts) | **GET** /v1/crm/{accountId}/contacts/search | Search CRM contacts
[**update_crm_contact**](CrmApi.md#update_crm_contact) | **PATCH** /v1/crm/{accountId}/contacts/{contactId} | Update a CRM contact
[**update_crm_deal**](CrmApi.md#update_crm_deal) | **PATCH** /v1/crm/{accountId}/deals/{dealId} | Update a CRM deal



## create_crm_activity

> models::CreateCrmActivity201Response create_crm_activity(account_id, contact_id, create_crm_activity_request)
Log a CRM activity

Log something that happened with a person on their CRM record.  - HubSpot: a Communication on the contact's timeline for `channel` `whatsapp` or `sms`, otherwise a Note. The subject and direction lead the text. - Salesforce: a completed Task on the Contact or Lead (`WhoId`), dated `occurredAt`, with `body` as its comments. `channel: call` logs a call.  To log inbox conversations automatically instead, turn on `logMessages` in the CRM settings.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The connected HubSpot or Salesforce account (`GET /v1/accounts?platform=hubspot` or `salesforce`). | [required] |
**contact_id** | **String** | The CRM's own id. HubSpot contact id, or Salesforce Contact (`003...`) or Lead (`00Q...`) id. | [required] |
**create_crm_activity_request** | [**CreateCrmActivityRequest**](CreateCrmActivityRequest.md) |  | [required] |

### Return type

[**models::CreateCrmActivity201Response**](createCrmActivity_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_crm_contact

> models::CreateCrmContact201Response create_crm_contact(account_id, create_crm_contact_request)
Create a CRM contact

Create a person in the connected CRM. HubSpot creates a contact. Salesforce creates a Lead or a Contact: `createAs`, else the connection's `createAs` setting (default `lead`).  Salesforce requires `lastName` on both, and `company` on a Lead (`[not provided]` when you send none). A Contact takes its company from its Account: set `properties.AccountId` instead.  Anything the CRM refuses (a required field, a validation rule, a duplicate rule) comes back as 422 or 409 with the CRM's own errors in `details.errors`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The connected HubSpot or Salesforce account (`GET /v1/accounts?platform=hubspot` or `salesforce`). | [required] |
**create_crm_contact_request** | [**CreateCrmContactRequest**](CreateCrmContactRequest.md) |  | [required] |

### Return type

[**models::CreateCrmContact201Response**](createCrmContact_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_crm_contact

> models::CreateCrmContact201Response get_crm_contact(account_id, contact_id, properties, include_raw)
Get a CRM contact

Read one person from the connected CRM. On Salesforce the id can be a Contact (`003...`) or a Lead (`00Q...`).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The connected HubSpot or Salesforce account (`GET /v1/accounts?platform=hubspot` or `salesforce`). | [required] |
**contact_id** | **String** | The CRM's own id. HubSpot contact id, or Salesforce Contact (`003...`) or Lead (`00Q...`) id. | [required] |
**properties** | Option<**String**> | Comma-separated native field names to return in `properties` (at most 50), for example `lifecyclestage,hs_lead_status` or `LeadSource,Industry__c`. |  |
**include_raw** | Option<**bool**> | Also return the CRM's own record as `raw`. |  |[default to false]

### Return type

[**models::CreateCrmContact201Response**](createCrmContact_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_crm_deal

> models::GetCrmDeal200Response get_crm_deal(account_id, deal_id, properties, include_raw)
Get a CRM deal

Read one deal (HubSpot) or Opportunity (Salesforce) with its contacts.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The connected HubSpot or Salesforce account (`GET /v1/accounts?platform=hubspot` or `salesforce`). | [required] |
**deal_id** | **String** | HubSpot deal id or Salesforce Opportunity id (`006...`). | [required] |
**properties** | Option<**String**> | Comma-separated native field names to return in `properties` (at most 50), for example `lifecyclestage,hs_lead_status` or `LeadSource,Industry__c`. |  |
**include_raw** | Option<**bool**> | Also return the CRM's own record as `raw`. |  |[default to false]

### Return type

[**models::GetCrmDeal200Response**](getCrmDeal_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_crm_deals

> models::ListCrmDeals200Response list_crm_deals(account_id, stage, updated_since, properties, include_raw, limit, cursor)
List CRM deals

List deals (HubSpot) or Opportunities (Salesforce), most recently changed first.  HubSpot needs the portal to have granted `crm.objects.deals.read`; otherwise 403 `crm_scope_missing`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The connected HubSpot or Salesforce account (`GET /v1/accounts?platform=hubspot` or `salesforce`). | [required] |
**stage** | Option<**String**> | Only deals in this stage. HubSpot takes the stage's internal id (`closedwon`, `appointmentscheduled`); Salesforce the `StageName` (`Closed Won`). |  |
**updated_since** | Option<**String**> | Only deals changed at or after this time. |  |
**properties** | Option<**String**> | Comma-separated native field names to return in `properties` (at most 50), for example `lifecyclestage,hs_lead_status` or `LeadSource,Industry__c`. |  |
**include_raw** | Option<**bool**> | Also return the CRM's own record as `raw`. |  |[default to false]
**limit** | Option<**i32**> |  |  |[default to 25]
**cursor** | Option<**String**> | The `nextCursor` of the previous page, unchanged. |  |

### Return type

[**models::ListCrmDeals200Response**](listCrmDeals_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_crm_owners

> models::ListCrmOwners200Response list_crm_owners(account_id, include_raw, limit, cursor)
List CRM owners

List the users records can be assigned to: HubSpot owners, or active standard Salesforce users. Use an `id` as `ownerId` on contacts and deals.  HubSpot needs `crm.objects.owners.read`, an optional scope portals approve when they connect; without it, 403 `crm_scope_missing` asks to reconnect HubSpot.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The connected HubSpot or Salesforce account (`GET /v1/accounts?platform=hubspot` or `salesforce`). | [required] |
**include_raw** | Option<**bool**> | Also return the CRM's own record as `raw`. |  |[default to false]
**limit** | Option<**i32**> |  |  |[default to 25]
**cursor** | Option<**String**> | The `nextCursor` of the previous page, unchanged. |  |

### Return type

[**models::ListCrmOwners200Response**](listCrmOwners_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## search_crm_contacts

> models::SearchCrmContacts200Response search_crm_contacts(account_id, q, email, phone, properties, include_raw, limit, cursor)
Search CRM contacts

Find people in the connected CRM by free text, email or phone. Send exactly one of `q`, `email` or `phone`.  HubSpot searches contacts. Salesforce searches Contacts and Leads that are not converted (`objectType` tells which), newest change first.  - `email` is an exact match. - `phone` takes an international number and matches it however the CRM stored it (\"+44 7911 123456\", \"07911 123456\"). - `q` searches names, emails, phones and company. On Salesforce, `q` and `phone` use the search index, so a record saved in the last few minutes may not show yet; `email` never lags.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The connected HubSpot or Salesforce account (`GET /v1/accounts?platform=hubspot` or `salesforce`). | [required] |
**q** | Option<**String**> | Free text, at least 2 characters. |  |
**email** | Option<**String**> |  |  |
**phone** | Option<**String**> | International number with its country code, for example `+14155550100`. |  |
**properties** | Option<**String**> | Comma-separated native field names to return in `properties` (at most 50), for example `lifecyclestage,hs_lead_status` or `LeadSource,Industry__c`. |  |
**include_raw** | Option<**bool**> | Also return the CRM's own record as `raw`. |  |[default to false]
**limit** | Option<**i32**> |  |  |[default to 25]
**cursor** | Option<**String**> | The `nextCursor` of the previous page, unchanged. |  |

### Return type

[**models::SearchCrmContacts200Response**](searchCrmContacts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_crm_contact

> models::CreateCrmContact201Response update_crm_contact(account_id, contact_id, crm_contact_input)
Update a CRM contact

Change fields on a person in the connected CRM. Send only what changes; `null` clears a field. Native fields go in `properties`.  On Salesforce, `company` applies to Leads only (400 on a Contact).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The connected HubSpot or Salesforce account (`GET /v1/accounts?platform=hubspot` or `salesforce`). | [required] |
**contact_id** | **String** | The CRM's own id. HubSpot contact id, or Salesforce Contact (`003...`) or Lead (`00Q...`) id. | [required] |
**crm_contact_input** | [**CrmContactInput**](CrmContactInput.md) |  | [required] |

### Return type

[**models::CreateCrmContact201Response**](createCrmContact_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_crm_deal

> models::GetCrmDeal200Response update_crm_deal(account_id, deal_id, update_crm_deal_request)
Update a CRM deal

Move a deal to another stage, or change its amount, close date, owner or native fields. Send only what changes.  HubSpot needs `crm.objects.deals.write`, an optional scope portals approve when they connect; without it, 403 `crm_scope_missing` asks to reconnect HubSpot. `currency` only works on multi-currency HubSpot portals and Salesforce orgs.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The connected HubSpot or Salesforce account (`GET /v1/accounts?platform=hubspot` or `salesforce`). | [required] |
**deal_id** | **String** | HubSpot deal id or Salesforce Opportunity id (`006...`). | [required] |
**update_crm_deal_request** | [**UpdateCrmDealRequest**](UpdateCrmDealRequest.md) |  | [required] |

### Return type

[**models::GetCrmDeal200Response**](getCrmDeal_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

