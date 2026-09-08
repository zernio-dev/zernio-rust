# \BusinessAgentApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_business_agent_allowlist_entry**](BusinessAgentApi.md#add_business_agent_allowlist_entry) | **POST** /v1/accounts/{accountId}/business-agent/allowlist | Allowlist a consumer
[**add_business_agent_website**](BusinessAgentApi.md#add_business_agent_website) | **POST** /v1/accounts/{accountId}/business-agent/websites | Add a website to crawl
[**create_business_agent_connector**](BusinessAgentApi.md#create_business_agent_connector) | **POST** /v1/accounts/{accountId}/business-agent/connectors | Create a connector
[**create_business_agent_connector_tool**](BusinessAgentApi.md#create_business_agent_connector_tool) | **POST** /v1/accounts/{accountId}/business-agent/connectors/{connectorId}/tools | Create a connector tool
[**create_business_agent_faq**](BusinessAgentApi.md#create_business_agent_faq) | **POST** /v1/accounts/{accountId}/business-agent/faqs | Create a FAQ
[**create_business_agent_skill**](BusinessAgentApi.md#create_business_agent_skill) | **POST** /v1/accounts/{accountId}/business-agent/skills | Create a skill
[**create_business_agent_ui_skill**](BusinessAgentApi.md#create_business_agent_ui_skill) | **POST** /v1/accounts/{accountId}/business-agent/ui-skills | Create a UI skill
[**delete_business_agent_connector**](BusinessAgentApi.md#delete_business_agent_connector) | **DELETE** /v1/accounts/{accountId}/business-agent/connectors/{connectorId} | Delete a connector
[**delete_business_agent_connector_tool**](BusinessAgentApi.md#delete_business_agent_connector_tool) | **DELETE** /v1/accounts/{accountId}/business-agent/connectors/{connectorId}/tools/{toolId} | Delete a connector tool
[**delete_business_agent_faq**](BusinessAgentApi.md#delete_business_agent_faq) | **DELETE** /v1/accounts/{accountId}/business-agent/faqs/{faqId} | Delete a FAQ
[**delete_business_agent_file**](BusinessAgentApi.md#delete_business_agent_file) | **DELETE** /v1/accounts/{accountId}/business-agent/files/{fileId} | Delete a knowledge file
[**delete_business_agent_skill**](BusinessAgentApi.md#delete_business_agent_skill) | **DELETE** /v1/accounts/{accountId}/business-agent/skills/{skillId} | Delete a skill
[**delete_business_agent_ui_skill**](BusinessAgentApi.md#delete_business_agent_ui_skill) | **DELETE** /v1/accounts/{accountId}/business-agent/ui-skills/{uiSkillId} | Delete a UI skill
[**delete_business_agent_website**](BusinessAgentApi.md#delete_business_agent_website) | **DELETE** /v1/accounts/{accountId}/business-agent/websites/{websiteId} | Remove a crawled website
[**get_business_agent_budget**](BusinessAgentApi.md#get_business_agent_budget) | **GET** /v1/accounts/{accountId}/business-agent/budget | Get usage budgets
[**get_business_agent_business_information**](BusinessAgentApi.md#get_business_agent_business_information) | **GET** /v1/accounts/{accountId}/business-agent/business-information | Get business information
[**get_business_agent_connector**](BusinessAgentApi.md#get_business_agent_connector) | **GET** /v1/accounts/{accountId}/business-agent/connectors/{connectorId} | Get a connector
[**get_business_agent_connector_logs**](BusinessAgentApi.md#get_business_agent_connector_logs) | **GET** /v1/accounts/{accountId}/business-agent/connectors/{connectorId}/logs | Get connector failure logs
[**get_business_agent_connector_tool**](BusinessAgentApi.md#get_business_agent_connector_tool) | **GET** /v1/accounts/{accountId}/business-agent/connectors/{connectorId}/tools/{toolId} | Get a connector tool
[**get_business_agent_event**](BusinessAgentApi.md#get_business_agent_event) | **GET** /v1/accounts/{accountId}/business-agent/events/{eventId} | Get a business event status
[**get_business_agent_faq**](BusinessAgentApi.md#get_business_agent_faq) | **GET** /v1/accounts/{accountId}/business-agent/faqs/{faqId} | Get a FAQ
[**get_business_agent_file**](BusinessAgentApi.md#get_business_agent_file) | **GET** /v1/accounts/{accountId}/business-agent/files/{fileId} | Get a knowledge file
[**get_business_agent_skill**](BusinessAgentApi.md#get_business_agent_skill) | **GET** /v1/accounts/{accountId}/business-agent/skills/{skillId} | Get a skill
[**get_business_agent_status**](BusinessAgentApi.md#get_business_agent_status) | **GET** /v1/accounts/{accountId}/business-agent | Get agent setup status
[**get_business_agent_ui_skill**](BusinessAgentApi.md#get_business_agent_ui_skill) | **GET** /v1/accounts/{accountId}/business-agent/ui-skills/{uiSkillId} | Get a UI skill
[**get_business_agent_website**](BusinessAgentApi.md#get_business_agent_website) | **GET** /v1/accounts/{accountId}/business-agent/websites/{websiteId} | Get a crawled website
[**list_business_agent_allowlist**](BusinessAgentApi.md#list_business_agent_allowlist) | **GET** /v1/accounts/{accountId}/business-agent/allowlist | List allowlisted consumers
[**list_business_agent_connector_tools**](BusinessAgentApi.md#list_business_agent_connector_tools) | **GET** /v1/accounts/{accountId}/business-agent/connectors/{connectorId}/tools | List connector tools
[**list_business_agent_connectors**](BusinessAgentApi.md#list_business_agent_connectors) | **GET** /v1/accounts/{accountId}/business-agent/connectors | List connectors
[**list_business_agent_faqs**](BusinessAgentApi.md#list_business_agent_faqs) | **GET** /v1/accounts/{accountId}/business-agent/faqs | List FAQs
[**list_business_agent_files**](BusinessAgentApi.md#list_business_agent_files) | **GET** /v1/accounts/{accountId}/business-agent/files | List knowledge files
[**list_business_agent_settings**](BusinessAgentApi.md#list_business_agent_settings) | **GET** /v1/accounts/{accountId}/business-agent/settings | List agent settings
[**list_business_agent_skills**](BusinessAgentApi.md#list_business_agent_skills) | **GET** /v1/accounts/{accountId}/business-agent/skills | List skills
[**list_business_agent_ui_skills**](BusinessAgentApi.md#list_business_agent_ui_skills) | **GET** /v1/accounts/{accountId}/business-agent/ui-skills | List UI skills
[**list_business_agent_websites**](BusinessAgentApi.md#list_business_agent_websites) | **GET** /v1/accounts/{accountId}/business-agent/websites | List crawled websites
[**onboard_business_agent**](BusinessAgentApi.md#onboard_business_agent) | **POST** /v1/accounts/{accountId}/business-agent/onboard | Create the agent
[**read_business_agent_evals**](BusinessAgentApi.md#read_business_agent_evals) | **GET** /v1/accounts/{accountId}/business-agent/evals | Read evaluation data
[**refresh_business_agent_connector_tools**](BusinessAgentApi.md#refresh_business_agent_connector_tools) | **POST** /v1/accounts/{accountId}/business-agent/connectors/{connectorId}/refresh-tools | Refresh MCP connector tools
[**remove_business_agent_allowlist_entry**](BusinessAgentApi.md#remove_business_agent_allowlist_entry) | **DELETE** /v1/accounts/{accountId}/business-agent/allowlist/{entryId} | Remove an allowlisted consumer
[**replace_business_agent_budget**](BusinessAgentApi.md#replace_business_agent_budget) | **PUT** /v1/accounts/{accountId}/business-agent/budget | Replace usage budgets
[**replace_business_agent_business_information**](BusinessAgentApi.md#replace_business_agent_business_information) | **PUT** /v1/accounts/{accountId}/business-agent/business-information | Replace business information
[**reset_business_agent_business_information**](BusinessAgentApi.md#reset_business_agent_business_information) | **DELETE** /v1/accounts/{accountId}/business-agent/business-information | Reset business information
[**run_business_agent_connector_tool**](BusinessAgentApi.md#run_business_agent_connector_tool) | **POST** /v1/accounts/{accountId}/business-agent/connectors/{connectorId}/tools/{toolId}/run | Run a connector tool once
[**send_business_agent_event**](BusinessAgentApi.md#send_business_agent_event) | **POST** /v1/accounts/{accountId}/business-agent/events | Send a business event
[**send_business_agent_test_message**](BusinessAgentApi.md#send_business_agent_test_message) | **POST** /v1/accounts/{accountId}/business-agent/test-messages | Send a test message
[**set_business_agent_connector_credentials**](BusinessAgentApi.md#set_business_agent_connector_credentials) | **POST** /v1/accounts/{accountId}/business-agent/connectors/{connectorId}/credentials | Set connector credentials
[**start_business_agent_eval_run**](BusinessAgentApi.md#start_business_agent_eval_run) | **POST** /v1/accounts/{accountId}/business-agent/evals | Start an evaluation run
[**update_business_agent_connector**](BusinessAgentApi.md#update_business_agent_connector) | **PUT** /v1/accounts/{accountId}/business-agent/connectors/{connectorId} | Update a connector
[**update_business_agent_connector_tool**](BusinessAgentApi.md#update_business_agent_connector_tool) | **PUT** /v1/accounts/{accountId}/business-agent/connectors/{connectorId}/tools/{toolId} | Update a connector tool
[**update_business_agent_faq**](BusinessAgentApi.md#update_business_agent_faq) | **PUT** /v1/accounts/{accountId}/business-agent/faqs/{faqId} | Update a FAQ
[**update_business_agent_settings**](BusinessAgentApi.md#update_business_agent_settings) | **PATCH** /v1/accounts/{accountId}/business-agent/settings | Update agent settings
[**update_business_agent_skill**](BusinessAgentApi.md#update_business_agent_skill) | **PUT** /v1/accounts/{accountId}/business-agent/skills/{skillId} | Update a skill
[**update_business_agent_ui_skill**](BusinessAgentApi.md#update_business_agent_ui_skill) | **PUT** /v1/accounts/{accountId}/business-agent/ui-skills/{uiSkillId} | Update a UI skill
[**update_business_agent_website**](BusinessAgentApi.md#update_business_agent_website) | **PUT** /v1/accounts/{accountId}/business-agent/websites/{websiteId} | Update a crawled website
[**upload_business_agent_file**](BusinessAgentApi.md#upload_business_agent_file) | **POST** /v1/accounts/{accountId}/business-agent/files | Upload a knowledge file



## add_business_agent_allowlist_entry

> models::BusinessAgentAllowlistEntry add_business_agent_allowlist_entry(account_id, add_business_agent_allowlist_entry_request)
Allowlist a consumer

One E.164 number per call. Not idempotent.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**add_business_agent_allowlist_entry_request** | [**AddBusinessAgentAllowlistEntryRequest**](AddBusinessAgentAllowlistEntryRequest.md) |  | [required] |

### Return type

[**models::BusinessAgentAllowlistEntry**](BusinessAgentAllowlistEntry.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## add_business_agent_website

> models::BusinessAgentWebsite add_business_agent_website(account_id, business_agent_website_input)
Add a website to crawl

Meta crawls the site into the agent knowledge and recrawls it periodically; check `crawl_status` and `crawl_error` on read. Not idempotent.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**business_agent_website_input** | [**BusinessAgentWebsiteInput**](BusinessAgentWebsiteInput.md) |  | [required] |

### Return type

[**models::BusinessAgentWebsite**](BusinessAgentWebsite.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_business_agent_connector

> models::BusinessAgentConnector create_business_agent_connector(account_id, business_agent_connector_input)
Create a connector

Base URL plus how to authenticate (OAuth client credentials, API key or none). Names are unique per number. Not idempotent.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**business_agent_connector_input** | [**BusinessAgentConnectorInput**](BusinessAgentConnectorInput.md) |  | [required] |

### Return type

[**models::BusinessAgentConnector**](BusinessAgentConnector.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_business_agent_connector_tool

> models::BusinessAgentConnectorTool create_business_agent_connector_tool(account_id, connector_id, business_agent_connector_tool_input)
Create a connector tool

One operation on the connector, with the request definition Meta uses to build the outbound call from the conversation. Type the body params explicitly. Not idempotent.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**connector_id** | **String** |  | [required] |
**business_agent_connector_tool_input** | [**BusinessAgentConnectorToolInput**](BusinessAgentConnectorToolInput.md) |  | [required] |

### Return type

[**models::BusinessAgentConnectorTool**](BusinessAgentConnectorTool.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_business_agent_faq

> models::BusinessAgentFaq create_business_agent_faq(account_id, business_agent_faq_input)
Create a FAQ

One specific question per entry; beyond a few hundred entries retrieval quality drops. Not idempotent.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**business_agent_faq_input** | [**BusinessAgentFaqInput**](BusinessAgentFaqInput.md) |  | [required] |

### Return type

[**models::BusinessAgentFaq**](BusinessAgentFaq.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_business_agent_skill

> models::BusinessAgentSkill create_business_agent_skill(account_id, business_agent_skill_input)
Create a skill

Behavioral instructions in the brand voice. Reads back `pending_review` until Meta content review passes it. Not idempotent.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**business_agent_skill_input** | [**BusinessAgentSkillInput**](BusinessAgentSkillInput.md) |  | [required] |

### Return type

[**models::BusinessAgentSkill**](BusinessAgentSkill.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_business_agent_ui_skill

> models::BusinessAgentUiSkill create_business_agent_ui_skill(account_id, business_agent_ui_skill_input)
Create a UI skill

Tells the agent when to send a rich component (CTA URL button, image, carousel, list, reply buttons, location, Flow) and what to put in it. Not idempotent.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**business_agent_ui_skill_input** | [**BusinessAgentUiSkillInput**](BusinessAgentUiSkillInput.md) |  | [required] |

### Return type

[**models::BusinessAgentUiSkill**](BusinessAgentUiSkill.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_business_agent_connector

> models::InlineObject delete_business_agent_connector(account_id, connector_id)
Delete a connector

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**connector_id** | **String** |  | [required] |

### Return type

[**models::InlineObject**](inline_object.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_business_agent_connector_tool

> models::InlineObject delete_business_agent_connector_tool(account_id, connector_id, tool_id)
Delete a connector tool

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**connector_id** | **String** |  | [required] |
**tool_id** | **String** |  | [required] |

### Return type

[**models::InlineObject**](inline_object.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_business_agent_faq

> models::InlineObject delete_business_agent_faq(account_id, faq_id)
Delete a FAQ

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**faq_id** | **String** |  | [required] |

### Return type

[**models::InlineObject**](inline_object.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_business_agent_file

> models::InlineObject delete_business_agent_file(account_id, file_id)
Delete a knowledge file

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**file_id** | **String** |  | [required] |

### Return type

[**models::InlineObject**](inline_object.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_business_agent_skill

> models::InlineObject delete_business_agent_skill(account_id, skill_id)
Delete a skill

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**skill_id** | **String** |  | [required] |

### Return type

[**models::InlineObject**](inline_object.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_business_agent_ui_skill

> models::InlineObject delete_business_agent_ui_skill(account_id, ui_skill_id)
Delete a UI skill

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**ui_skill_id** | **String** |  | [required] |

### Return type

[**models::InlineObject**](inline_object.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_business_agent_website

> models::InlineObject delete_business_agent_website(account_id, website_id)
Remove a crawled website

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**website_id** | **String** |  | [required] |

### Return type

[**models::InlineObject**](inline_object.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_business_agent_budget

> models::GetBusinessAgentBudget200Response get_business_agent_budget(account_id)
Get usage budgets

Caps over rolling windows for the Business Manager that owns the number. An empty list means unlimited.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |

### Return type

[**models::GetBusinessAgentBudget200Response**](getBusinessAgentBudget_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_business_agent_business_information

> models::BusinessAgentBusinessInformation get_business_agent_business_information(account_id)
Get business information

Payment methods, return policy, how to buy, shipping, description and contact details the agent answers from. Empty values until configured.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |

### Return type

[**models::BusinessAgentBusinessInformation**](BusinessAgentBusinessInformation.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_business_agent_connector

> models::BusinessAgentConnector get_business_agent_connector(account_id, connector_id)
Get a connector

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**connector_id** | **String** |  | [required] |

### Return type

[**models::BusinessAgentConnector**](BusinessAgentConnector.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_business_agent_connector_logs

> models::GetBusinessAgentConnectorLogs200Response get_business_agent_connector_logs(account_id, connector_id, start_time, end_time, limit, tool_id, include_stats, summary_only, top_n)
Get connector failure logs

Third-party failures over the last 7 days (window at most 7 days, default the last 24 hours). Each entry carries `failure_code_name` and `error_message`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**connector_id** | **String** |  | [required] |
**start_time** | Option<**i32**> | Unix seconds. |  |
**end_time** | Option<**i32**> | Unix seconds. |  |
**limit** | Option<**i32**> |  |  |
**tool_id** | Option<**String**> |  |  |
**include_stats** | Option<**bool**> | Add success rate and latency percentiles. |  |
**summary_only** | Option<**bool**> | Aggregate failure patterns instead of entries. |  |
**top_n** | Option<**i32**> |  |  |

### Return type

[**models::GetBusinessAgentConnectorLogs200Response**](getBusinessAgentConnectorLogs_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_business_agent_connector_tool

> models::BusinessAgentConnectorTool get_business_agent_connector_tool(account_id, connector_id, tool_id)
Get a connector tool

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**connector_id** | **String** |  | [required] |
**tool_id** | **String** |  | [required] |

### Return type

[**models::BusinessAgentConnectorTool**](BusinessAgentConnectorTool.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_business_agent_event

> models::BusinessAgentEventStatus get_business_agent_event(account_id, event_id)
Get a business event status

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**event_id** | **String** |  | [required] |

### Return type

[**models::BusinessAgentEventStatus**](BusinessAgentEventStatus.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_business_agent_faq

> models::BusinessAgentFaq get_business_agent_faq(account_id, faq_id)
Get a FAQ

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**faq_id** | **String** |  | [required] |

### Return type

[**models::BusinessAgentFaq**](BusinessAgentFaq.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_business_agent_file

> models::BusinessAgentKnowledgeFile get_business_agent_file(account_id, file_id)
Get a knowledge file

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**file_id** | **String** |  | [required] |

### Return type

[**models::BusinessAgentKnowledgeFile**](BusinessAgentKnowledgeFile.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_business_agent_skill

> models::BusinessAgentSkill get_business_agent_skill(account_id, skill_id)
Get a skill

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**skill_id** | **String** |  | [required] |

### Return type

[**models::BusinessAgentSkill**](BusinessAgentSkill.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_business_agent_status

> models::BusinessAgentStatus get_business_agent_status(account_id)
Get agent setup status

One read that says where the merchant is: whether the number is eligible, whether the Meta Business Agent terms are accepted, whether an agent exists, whether it is on, and its settings. `manualSteps` lists what Zernio can verify is still pending (accepting the terms in WhatsApp Manager); `unverifiedSteps` lists what Meta exposes no state for (the payment method in Billing Hub). Never fails for those pre-setup states; it reports them as flags. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |

### Return type

[**models::BusinessAgentStatus**](BusinessAgentStatus.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_business_agent_ui_skill

> models::BusinessAgentUiSkill get_business_agent_ui_skill(account_id, ui_skill_id)
Get a UI skill

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**ui_skill_id** | **String** |  | [required] |

### Return type

[**models::BusinessAgentUiSkill**](BusinessAgentUiSkill.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_business_agent_website

> models::BusinessAgentWebsite get_business_agent_website(account_id, website_id)
Get a crawled website

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**website_id** | **String** |  | [required] |

### Return type

[**models::BusinessAgentWebsite**](BusinessAgentWebsite.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_business_agent_allowlist

> models::ListBusinessAgentAllowlist200Response list_business_agent_allowlist(account_id)
List allowlisted consumers

Consumers the agent answers while `ai_audience` is ALLOWLISTED_ONLY.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |

### Return type

[**models::ListBusinessAgentAllowlist200Response**](listBusinessAgentAllowlist_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_business_agent_connector_tools

> models::ListBusinessAgentConnectorTools200Response list_business_agent_connector_tools(account_id, connector_id)
List connector tools

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**connector_id** | **String** |  | [required] |

### Return type

[**models::ListBusinessAgentConnectorTools200Response**](listBusinessAgentConnectorTools_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_business_agent_connectors

> models::ListBusinessAgentConnectors200Response list_business_agent_connectors(account_id)
List connectors

External APIs the agent may call. `connection_status` says whether Meta can currently reach each one.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |

### Return type

[**models::ListBusinessAgentConnectors200Response**](listBusinessAgentConnectors_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_business_agent_faqs

> models::ListBusinessAgentFaqs200Response list_business_agent_faqs(account_id)
List FAQs

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |

### Return type

[**models::ListBusinessAgentFaqs200Response**](listBusinessAgentFaqs_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_business_agent_files

> models::ListBusinessAgentFiles200Response list_business_agent_files(account_id)
List knowledge files

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |

### Return type

[**models::ListBusinessAgentFiles200Response**](listBusinessAgentFiles_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_business_agent_settings

> models::ListBusinessAgentSettings200Response list_business_agent_settings(account_id, agent_id)
List agent settings

Settings of every agent configured on the number (normally one). Pass `agentId` to read one.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**agent_id** | Option<**String**> |  |  |

### Return type

[**models::ListBusinessAgentSettings200Response**](listBusinessAgentSettings_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_business_agent_skills

> models::ListBusinessAgentSkills200Response list_business_agent_skills(account_id)
List skills

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |

### Return type

[**models::ListBusinessAgentSkills200Response**](listBusinessAgentSkills_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_business_agent_ui_skills

> models::ListBusinessAgentUiSkills200Response list_business_agent_ui_skills(account_id, before, after, limit)
List UI skills

Cursor paged; follow `paging.cursors.after` until `paging.next` is absent.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**before** | Option<**String**> |  |  |
**after** | Option<**String**> |  |  |
**limit** | Option<**i32**> |  |  |

### Return type

[**models::ListBusinessAgentUiSkills200Response**](listBusinessAgentUiSkills_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_business_agent_websites

> models::ListBusinessAgentWebsites200Response list_business_agent_websites(account_id)
List crawled websites

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |

### Return type

[**models::ListBusinessAgentWebsites200Response**](listBusinessAgentWebsites_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## onboard_business_agent

> models::OnboardBusinessAgent201Response onboard_business_agent(account_id)
Create the agent

Creates the Meta Business Agent on the number and schedules Meta's data preparation. Requires the terms to be accepted; eligibility is checked first and an ineligible number answers 403 `business_agent_not_eligible`. Not idempotent: call it once, then configure knowledge and skills, then enable it through the settings. Configuration calls made in the first minute can still answer `business_agent_not_found` while Meta prepares the workspace. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |

### Return type

[**models::OnboardBusinessAgent201Response**](onboardBusinessAgent_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## read_business_agent_evals

> std::collections::HashMap<String, serde_json::Value> read_business_agent_evals(account_id, job_id, summary_ids, eval_ids)
Read evaluation data

Without query parameters, lists the evaluation scenarios (`eval_cases`). With `jobId`, polls a run started with POST. With `summaryIds`, returns the aggregated insight reports. With `evalIds`, returns per-conversation evaluation details. One of the three at a time. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**job_id** | Option<**String**> |  |  |
**summary_ids** | Option<**String**> | Comma-separated summary ids. |  |
**eval_ids** | Option<**String**> | Comma-separated evaluation ids. |  |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## refresh_business_agent_connector_tools

> models::BusinessAgentConnector refresh_business_agent_connector_tools(account_id, connector_id)
Refresh MCP connector tools

Re-discovers the tools of an MCP connector. A failed discovery keeps the previous tool set and reports an ERROR sync status inside a 200.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**connector_id** | **String** |  | [required] |

### Return type

[**models::BusinessAgentConnector**](BusinessAgentConnector.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_business_agent_allowlist_entry

> models::InlineObject remove_business_agent_allowlist_entry(account_id, entry_id)
Remove an allowlisted consumer

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**entry_id** | **String** |  | [required] |

### Return type

[**models::InlineObject**](inline_object.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## replace_business_agent_budget

> models::GetBusinessAgentBudget200Response replace_business_agent_budget(account_id, get_business_agent_budget200_response)
Replace usage budgets

The full desired set: budgets left out are removed, an empty list returns to unlimited. Pass `budget_id` to edit one in place. When a cap is hit the agent finishes its turn, stops answering and hands the thread to a human until the window rolls over.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**get_business_agent_budget200_response** | [**GetBusinessAgentBudget200Response**](GetBusinessAgentBudget200Response.md) |  | [required] |

### Return type

[**models::GetBusinessAgentBudget200Response**](getBusinessAgentBudget_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## replace_business_agent_business_information

> models::BusinessAgentBusinessInformation replace_business_agent_business_information(account_id, business_agent_business_information)
Replace business information

Full replacement: every field you send overwrites the stored value; fields you omit are cleared.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**business_agent_business_information** | [**BusinessAgentBusinessInformation**](BusinessAgentBusinessInformation.md) |  | [required] |

### Return type

[**models::BusinessAgentBusinessInformation**](BusinessAgentBusinessInformation.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reset_business_agent_business_information

> models::InlineObject reset_business_agent_business_information(account_id)
Reset business information

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |

### Return type

[**models::InlineObject**](inline_object.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## run_business_agent_connector_tool

> models::RunBusinessAgentConnectorTool200Response run_business_agent_connector_tool(account_id, connector_id, tool_id, run_business_agent_connector_tool_request)
Run a connector tool once

Executes the tool against the merchant API and returns the raw upstream result, to check a connector before the agent relies on it.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**connector_id** | **String** |  | [required] |
**tool_id** | **String** |  | [required] |
**run_business_agent_connector_tool_request** | [**RunBusinessAgentConnectorToolRequest**](RunBusinessAgentConnectorToolRequest.md) |  | [required] |

### Return type

[**models::RunBusinessAgentConnectorTool200Response**](runBusinessAgentConnectorTool_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## send_business_agent_event

> models::SendBusinessAgentEvent202Response send_business_agent_event(account_id, send_business_agent_event_request)
Send a business event

Tell the agent something happened in your systems (order shipped, document verified) so it messages the consumer about it. The consumer must already have a conversation with the number. Answers 202 with the event id; poll it for the outcome.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**send_business_agent_event_request** | [**SendBusinessAgentEventRequest**](SendBusinessAgentEventRequest.md) |  | [required] |

### Return type

[**models::SendBusinessAgentEvent202Response**](sendBusinessAgentEvent_202_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## send_business_agent_test_message

> models::BusinessAgentTestMessageResponse send_business_agent_test_message(account_id, send_business_agent_test_message_request)
Send a test message

Runs the message through the full agent pipeline in Meta sandbox with no WhatsApp user and no token billing. Pass back `conversationId` to continue a thread. Meta rate-limits it per number per hour.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**send_business_agent_test_message_request** | [**SendBusinessAgentTestMessageRequest**](SendBusinessAgentTestMessageRequest.md) |  | [required] |

### Return type

[**models::BusinessAgentTestMessageResponse**](BusinessAgentTestMessageResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## set_business_agent_connector_credentials

> models::BusinessAgentConnector set_business_agent_connector_credentials(account_id, connector_id, set_business_agent_connector_credentials_request)
Set connector credentials

Set or rotate the connector's credentials in place: `kind: api_key`, `kind: oauth` (client credentials) or `kind: certificate` (mTLS client certificate). Meta has no call that removes a credential layer; change the connector's `auth_type` or delete it instead. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**connector_id** | **String** |  | [required] |
**set_business_agent_connector_credentials_request** | [**SetBusinessAgentConnectorCredentialsRequest**](SetBusinessAgentConnectorCredentialsRequest.md) |  | [required] |

### Return type

[**models::BusinessAgentConnector**](BusinessAgentConnector.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## start_business_agent_eval_run

> models::StartBusinessAgentEvalRun202Response start_business_agent_eval_run(account_id, start_business_agent_eval_run_request)
Start an evaluation run

Simulates the given scenarios against the agent and scores them. Answers 202 with a `job_id` to poll with GET.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**start_business_agent_eval_run_request** | [**StartBusinessAgentEvalRunRequest**](StartBusinessAgentEvalRunRequest.md) |  | [required] |

### Return type

[**models::StartBusinessAgentEvalRun202Response**](startBusinessAgentEvalRun_202_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_business_agent_connector

> models::BusinessAgentConnector update_business_agent_connector(account_id, connector_id, business_agent_connector_input)
Update a connector

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**connector_id** | **String** |  | [required] |
**business_agent_connector_input** | [**BusinessAgentConnectorInput**](BusinessAgentConnectorInput.md) |  | [required] |

### Return type

[**models::BusinessAgentConnector**](BusinessAgentConnector.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_business_agent_connector_tool

> models::BusinessAgentConnectorTool update_business_agent_connector_tool(account_id, connector_id, tool_id, business_agent_connector_tool_input)
Update a connector tool

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**connector_id** | **String** |  | [required] |
**tool_id** | **String** |  | [required] |
**business_agent_connector_tool_input** | [**BusinessAgentConnectorToolInput**](BusinessAgentConnectorToolInput.md) |  | [required] |

### Return type

[**models::BusinessAgentConnectorTool**](BusinessAgentConnectorTool.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_business_agent_faq

> models::BusinessAgentFaq update_business_agent_faq(account_id, faq_id, business_agent_faq_input)
Update a FAQ

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**faq_id** | **String** |  | [required] |
**business_agent_faq_input** | [**BusinessAgentFaqInput**](BusinessAgentFaqInput.md) |  | [required] |

### Return type

[**models::BusinessAgentFaq**](BusinessAgentFaq.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_business_agent_settings

> models::BusinessAgentSettings update_business_agent_settings(account_id, update_business_agent_settings_request, agent_id)
Update agent settings

Partial update: fields you omit keep their value. `rollout.enabled: true` turns the agent on for new conversations; `false` stops it on every thread. Turning it on for `EVERYONE` needs a payment method on the Business Agent billable account (Meta accepts the call but delivers nothing without one); `ALLOWLISTED_ONLY` does not, which is how you test with a few numbers before billing. `never_say_phrases` replaces the whole list. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**update_business_agent_settings_request** | [**UpdateBusinessAgentSettingsRequest**](UpdateBusinessAgentSettingsRequest.md) |  | [required] |
**agent_id** | Option<**String**> |  |  |

### Return type

[**models::BusinessAgentSettings**](BusinessAgentSettings.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_business_agent_skill

> models::BusinessAgentSkill update_business_agent_skill(account_id, skill_id, business_agent_skill_input)
Update a skill

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**skill_id** | **String** |  | [required] |
**business_agent_skill_input** | [**BusinessAgentSkillInput**](BusinessAgentSkillInput.md) |  | [required] |

### Return type

[**models::BusinessAgentSkill**](BusinessAgentSkill.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_business_agent_ui_skill

> models::BusinessAgentUiSkill update_business_agent_ui_skill(account_id, ui_skill_id, business_agent_ui_skill_input)
Update a UI skill

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**ui_skill_id** | **String** |  | [required] |
**business_agent_ui_skill_input** | [**BusinessAgentUiSkillInput**](BusinessAgentUiSkillInput.md) |  | [required] |

### Return type

[**models::BusinessAgentUiSkill**](BusinessAgentUiSkill.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_business_agent_website

> models::BusinessAgentWebsite update_business_agent_website(account_id, website_id, business_agent_website_input)
Update a crawled website

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**website_id** | **String** |  | [required] |
**business_agent_website_input** | [**BusinessAgentWebsiteInput**](BusinessAgentWebsiteInput.md) |  | [required] |

### Return type

[**models::BusinessAgentWebsite**](BusinessAgentWebsite.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## upload_business_agent_file

> models::BusinessAgentKnowledgeFile upload_business_agent_file(account_id, upload_business_agent_file_request)
Upload a knowledge file

Accepted types: pdf, doc, docx, png, jpg, jpeg, plus csv and xlsx when Meta enabled extraction on the asset. Meta's limit is 100 MB. Two ways to send the file: - JSON `{ url, fileName }`: Zernio downloads the file (public https URL, no redirects,   capped at 100 MB) and forwards it. Use this for anything above a few megabytes. - multipart form-data with a `file` part (and an optional `fileName`): bounded by the   request body limit of about 4.5 MB; larger uploads must use the `url` form. Not idempotent. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account id (the number must be managed through the Cloud API). | [required] |
**upload_business_agent_file_request** | [**UploadBusinessAgentFileRequest**](UploadBusinessAgentFileRequest.md) |  | [required] |

### Return type

[**models::BusinessAgentKnowledgeFile**](BusinessAgentKnowledgeFile.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json, multipart/form-data
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

