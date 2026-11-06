# \AutomationsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**activate_automation**](AutomationsApi.md#activate_automation) | **POST** /v1/automations/{automationId}/activate | Turn an automation on
[**approve_automation_approval**](AutomationsApi.md#approve_automation_approval) | **POST** /v1/automations/{automationId}/approvals/{approvalId}/approve | Approve an approval request
[**backtest_automation**](AutomationsApi.md#backtest_automation) | **POST** /v1/automations/{automationId}/backtest | Backtest a saved automation
[**backtest_automation_draft**](AutomationsApi.md#backtest_automation_draft) | **POST** /v1/automations/backtest | Backtest an unsaved automation
[**create_automation**](AutomationsApi.md#create_automation) | **POST** /v1/automations | Create an automation
[**create_automation_template**](AutomationsApi.md#create_automation_template) | **POST** /v1/automations/templates | Create an automation template
[**delete_automation**](AutomationsApi.md#delete_automation) | **DELETE** /v1/automations/{automationId} | Delete an automation
[**delete_automation_template**](AutomationsApi.md#delete_automation_template) | **DELETE** /v1/automations/templates/{templateId} | Delete an automation template
[**get_automation**](AutomationsApi.md#get_automation) | **GET** /v1/automations/{automationId} | Get an automation
[**get_automation_approval**](AutomationsApi.md#get_automation_approval) | **GET** /v1/automations/{automationId}/approvals/{approvalId} | Get an approval request
[**get_automation_catalog**](AutomationsApi.md#get_automation_catalog) | **GET** /v1/automations/catalog | Get the automations catalog
[**get_automation_controls**](AutomationsApi.md#get_automation_controls) | **GET** /v1/automations/controls | Get automation controls
[**get_automation_template**](AutomationsApi.md#get_automation_template) | **GET** /v1/automations/templates/{templateId} | Get an automation template
[**get_shared_automation_template**](AutomationsApi.md#get_shared_automation_template) | **GET** /v1/automations/templates/shared/{shareToken} | Get a shared automation template
[**get_zernio_automation_template**](AutomationsApi.md#get_zernio_automation_template) | **GET** /v1/automations/templates/zernio/{templateId} | Get a Zernio automation template
[**install_automation_template**](AutomationsApi.md#install_automation_template) | **POST** /v1/automations/templates/{templateId}/install | Install an automation template
[**install_shared_automation_template**](AutomationsApi.md#install_shared_automation_template) | **POST** /v1/automations/templates/shared/{shareToken}/install | Install a shared automation template
[**install_zernio_automation_template**](AutomationsApi.md#install_zernio_automation_template) | **POST** /v1/automations/templates/zernio/{templateId}/install | Install a Zernio automation template
[**list_automation_actions**](AutomationsApi.md#list_automation_actions) | **GET** /v1/automations/actions | List automation actions
[**list_automation_approvals**](AutomationsApi.md#list_automation_approvals) | **GET** /v1/automations/{automationId}/approvals | List an automation's approval requests
[**list_automation_checks**](AutomationsApi.md#list_automation_checks) | **GET** /v1/automations/{automationId}/checks | List an automation's checks
[**list_automation_templates**](AutomationsApi.md#list_automation_templates) | **GET** /v1/automations/templates | List automation templates
[**list_automations**](AutomationsApi.md#list_automations) | **GET** /v1/automations | List automations
[**pause_automation**](AutomationsApi.md#pause_automation) | **POST** /v1/automations/{automationId}/pause | Turn an automation off
[**preview_automation**](AutomationsApi.md#preview_automation) | **POST** /v1/automations/{automationId}/preview | Preview a saved automation
[**preview_automation_draft**](AutomationsApi.md#preview_automation_draft) | **POST** /v1/automations/preview | Preview an unsaved automation
[**reject_automation_approval**](AutomationsApi.md#reject_automation_approval) | **POST** /v1/automations/{automationId}/approvals/{approvalId}/reject | Reject an approval request
[**update_automation**](AutomationsApi.md#update_automation) | **PATCH** /v1/automations/{automationId} | Edit an automation
[**update_automation_ad_account_controls**](AutomationsApi.md#update_automation_ad_account_controls) | **PATCH** /v1/automations/controls/ad-accounts | Update one ad account's controls
[**update_automation_controls**](AutomationsApi.md#update_automation_controls) | **PATCH** /v1/automations/controls | Turn every ad automation off or on
[**update_automation_template**](AutomationsApi.md#update_automation_template) | **PATCH** /v1/automations/templates/{templateId} | Update an automation template



## activate_automation

> models::CreateAutomation201Response activate_automation(automation_id)
Turn an automation on

An ad rule's first check runs right away.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**automation_id** | **String** |  | [required] |

### Return type

[**models::CreateAutomation201Response**](createAutomation_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## approve_automation_approval

> models::GetAutomationApproval200Response approve_automation_approval(automation_id, approval_id, automation_approval_decision)
Approve an approval request

Approves a pending request, so the automation acts on each change it holds. Each change is checked again first, and one that no longer applies is skipped.  Only the approvers the automation names now can decide, matched by the email of the user behind the API key. A request already decided, expired or cancelled is refused with nothing changed.  Each applied or failed change fires `automation.action.applied` or `automation.action.failed`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**automation_id** | **String** |  | [required] |
**approval_id** | **String** |  | [required] |
**automation_approval_decision** | Option<[**AutomationApprovalDecision**](AutomationApprovalDecision.md)> |  |  |

### Return type

[**models::GetAutomationApproval200Response**](getAutomationApproval_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## backtest_automation

> models::AutomationBacktest backtest_automation(automation_id, days)
Backtest a saved automation

What a saved automation would have done over the last `days` days, replayed on stored daily metrics. Nothing is changed.  Each day lists what it would have done. Its own changes carry into later days, but the metrics stay what really happened. `notes` says what the replay could not know.  Only ad automations can be backtested, on at most 5,000 ads. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**automation_id** | **String** |  | [required] |
**days** | Option<**i32**> | How many whole days before today to replay. Today is not replayed. |  |[default to 30]

### Return type

[**models::AutomationBacktest**](AutomationBacktest.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## backtest_automation_draft

> models::AutomationBacktest backtest_automation_draft(automation_definition, days)
Backtest an unsaved automation

Replays an automation over past days on stored daily metrics, without saving it or changing anything. It refuses what saving would refuse.  Each day lists what it would have done. Its own changes carry into later days, but the metrics stay what really happened. `notes` says what the replay could not know.  Only ad automations can be backtested, on at most 5,000 ads. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**automation_definition** | [**AutomationDefinition**](AutomationDefinition.md) |  | [required] |
**days** | Option<**i32**> | How many whole days before today to replay. Today is not replayed. |  |[default to 30]

### Return type

[**models::AutomationBacktest**](AutomationBacktest.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_automation

> models::CreateAutomation201Response create_automation(automation_definition, idempotency_key)
Create an automation

Creates an automation. Its shape picks the kind:  - **Ad rule**: a `schedule` over campaigns, ad sets or ads, with metric `conditions` and ad `steps`. It stays paused unless `status` is `active`; preview it first with `POST /v1/automations/preview`. - **Event**: a Zernio event in `trigger.type`, such as `post.failed`, with notify steps. It is on unless `status` is `paused`. - **Scheduled**: a `schedule` over a profile's posts, with notify steps and an optional boost. It is on unless `status` is `paused`.  Everything an automation cannot hold is refused at once: the 400 lists every problem with its JSON path in `details.problems`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**automation_definition** | [**AutomationDefinition**](AutomationDefinition.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  |  |

### Return type

[**models::CreateAutomation201Response**](createAutomation_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_automation_template

> models::CreateAutomationTemplate201Response create_automation_template(create_automation_template_request, idempotency_key)
Create an automation template

Saves a reusable setup of one or more automations (up to 20) that your team, or anyone you share it with, can install. Start from your own automations, one of Zernio's templates, a shared template, or definitions sent as they are.  Nothing tied to one account is kept. Ad accounts, a trigger's profile and accounts, and alert destinations become `inputs` that each install fills. Campaign ids, id filters, dates and approval steps are dropped.  From one of Zernio's templates, each threshold and budget or bid amount also becomes an input, with the template's own value as its default.  A template that would not install is refused: the 400 lists every problem in `details.problems`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_automation_template_request** | [**CreateAutomationTemplateRequest**](CreateAutomationTemplateRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  |  |

### Return type

[**models::CreateAutomationTemplate201Response**](createAutomationTemplate_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_automation

> models::UpdateYoutubeDefaultPlaylist200Response delete_automation(automation_id)
Delete an automation

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**automation_id** | **String** |  | [required] |

### Return type

[**models::UpdateYoutubeDefaultPlaylist200Response**](updateYoutubeDefaultPlaylist_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_automation_template

> models::DeleteAutomationTemplate200Response delete_automation_template(template_id)
Delete an automation template

Deletes one of your team's templates and its share link. Automations already installed from it stay. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**template_id** | **String** | The template's id. | [required] |

### Return type

[**models::DeleteAutomationTemplate200Response**](deleteAutomationTemplate_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_automation

> models::CreateAutomation201Response get_automation(automation_id)
Get an automation

An automation installed from a template also carries `template`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**automation_id** | **String** |  | [required] |

### Return type

[**models::CreateAutomation201Response**](createAutomation_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_automation_approval

> models::GetAutomationApproval200Response get_automation_approval(automation_id, approval_id)
Get an approval request

One approval request with the changes it holds, who may decide it and whether you can.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**automation_id** | **String** |  | [required] |
**approval_id** | **String** |  | [required] |

### Return type

[**models::GetAutomationApproval200Response**](getAutomationApproval_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_automation_catalog

> models::GetAutomationCatalog200Response get_automation_catalog()
Get the automations catalog

What an automation can contain and where each part works, built from the same checks that validate a save, so it never offers what saving refuses.  - `schema`: the JSON Schema of the body of `POST /v1/automations`. - `triggers`: every trigger, tagged with its `kind`. Ad rule and scheduled triggers list their intervals; event triggers list each event with its facts. - The other sections describe ad rules: per subject (campaign, ad set, ad) its metrics and steps with the platforms that accept them, plus filters, groups, alerts, conditions, limits and approval. 

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::GetAutomationCatalog200Response**](getAutomationCatalog_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_automation_controls

> models::GetAutomationControls200Response get_automation_controls()
Get automation controls

The team's switch for every ad rule, and each ad account's own switch and daily raise limit. Boosting automations do not read them.  Every team member sees the same controls. `adAccounts` lists each ad account your automations use, plus any ad account that has controls set. 

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::GetAutomationControls200Response**](getAutomationControls_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_automation_template

> models::CreateAutomationTemplate201Response get_automation_template(template_id)
Get an automation template

Returns one of your team's templates, with its inputs and automations. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**template_id** | **String** | The template's id. | [required] |

### Return type

[**models::CreateAutomationTemplate201Response**](createAutomationTemplate_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_shared_automation_template

> models::CreateAutomationTemplate201Response get_shared_automation_template(share_token)
Get a shared automation template

Returns a template shared by link, from any team. Who made it and its install counts in that team are left out, and `share` is null. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**share_token** | **String** | The token from the template's `share.token`. | [required] |

### Return type

[**models::CreateAutomationTemplate201Response**](createAutomationTemplate_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_zernio_automation_template

> models::CreateAutomationTemplate201Response get_zernio_automation_template(template_id)
Get a Zernio automation template

Returns one of Zernio's ready-made ad rule templates in the same shape as your own. Each threshold and budget or bid amount is an input with the template's own value as its default, so an install can change it or leave it. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**template_id** | **String** | The id of one of Zernio's templates, for example `stop_losers`. | [required] |

### Return type

[**models::CreateAutomationTemplate201Response**](createAutomationTemplate_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## install_automation_template

> models::AutomationTemplateInstallResponse install_automation_template(template_id, automation_template_install_request, idempotency_key)
Install an automation template

Creates every automation in the template, with your values in place of its inputs. All or nothing: if one automation fails, the ones already created are removed. New automations stay paused unless `status` is `active`.  To install on many ad accounts at once, send `targets` (up to 50). Each target is its own install with its own `inputs`, which win over the shared `inputs`. A failed target leaves the others in place, and the response is 207. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**template_id** | **String** | The template's id. | [required] |
**automation_template_install_request** | [**AutomationTemplateInstallRequest**](AutomationTemplateInstallRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  |  |

### Return type

[**models::AutomationTemplateInstallResponse**](AutomationTemplateInstallResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## install_shared_automation_template

> models::AutomationTemplateInstallResponse install_shared_automation_template(share_token, automation_template_install_request, idempotency_key)
Install a shared automation template

Installs a template shared by link into your account, the same way as your own templates.  To install on many ad accounts at once, send `targets` (up to 50). Each target is its own install with its own `inputs`, which win over the shared `inputs`. A failed target leaves the others in place, and the response is 207. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**share_token** | **String** | The token from the template's `share.token`. | [required] |
**automation_template_install_request** | [**AutomationTemplateInstallRequest**](AutomationTemplateInstallRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  |  |

### Return type

[**models::AutomationTemplateInstallResponse**](AutomationTemplateInstallResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## install_zernio_automation_template

> models::AutomationTemplateInstallResponse install_zernio_automation_template(template_id, automation_template_install_request, idempotency_key)
Install a Zernio automation template

Installs one of Zernio's ready-made templates. Leave a value input out to keep the template's default.  To install on many ad accounts at once, send `targets` (up to 50). Each target is its own install with its own `inputs`, which win over the shared `inputs`. A failed target leaves the others in place, and the response is 207. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**template_id** | **String** | The id of one of Zernio's templates, for example `stop_losers`. | [required] |
**automation_template_install_request** | [**AutomationTemplateInstallRequest**](AutomationTemplateInstallRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  |  |

### Return type

[**models::AutomationTemplateInstallResponse**](AutomationTemplateInstallResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_automation_actions

> models::ListAutomationActions200Response list_automation_actions(automation_id, account_id, r#type, from, to, limit, cursor)
List automation actions

Every change your ad rules made, newest first: what changed, the value before and after, and whether it was applied, skipped or failed. What event and scheduled automations did is in each one's checks. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**automation_id** | Option<**String**> |  |  |
**account_id** | Option<**String**> | Only actions on this ads connection. |  |
**r#type** | Option<**String**> | A change reads as the value it set, so budget changes filter as `ads.set_budget`. |  |
**from** | Option<**String**> |  |  |
**to** | Option<**String**> |  |  |
**limit** | Option<**i32**> |  |  |[default to 50]
**cursor** | Option<**String**> | `nextCursor` from the previous page. |  |

### Return type

[**models::ListAutomationActions200Response**](listAutomationActions_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_automation_approvals

> models::ListAutomationApprovals200Response list_automation_approvals(automation_id, status, limit)
List an automation's approval requests

The requests an automation sent for a person's approval before acting, newest first. Each lists the changes it holds, who may decide it and until when.  Only automations that ask for approval have requests. Others return 409. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**automation_id** | **String** |  | [required] |
**status** | Option<**String**> | Only requests in this status. |  |
**limit** | Option<**i32**> | How many requests to return. There is no cursor; the newest come first. |  |[default to 20]

### Return type

[**models::ListAutomationApprovals200Response**](listAutomationApprovals_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_automation_checks

> models::ListAutomationChecks200Response list_automation_checks(automation_id, limit, cursor)
List an automation's checks

Each time the automation ran, newest first, with what matched and what it did. For an event automation, each check is one event that reached it. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**automation_id** | **String** |  | [required] |
**limit** | Option<**i32**> |  |  |[default to 20]
**cursor** | Option<**String**> | `nextCursor` from the previous page. |  |

### Return type

[**models::ListAutomationChecks200Response**](listAutomationChecks_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_automation_templates

> models::ListAutomationTemplates200Response list_automation_templates(scope)
List automation templates

Lists your team's templates, newest first. Every team member sees the templates any member saved. A team keeps up to 200. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**scope** | Option<**String**> | Which templates to list. Only `team` today. |  |[default to team]

### Return type

[**models::ListAutomationTemplates200Response**](listAutomationTemplates_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_automations

> models::ListAutomations200Response list_automations(account_id, ad_account_id, limit, cursor)
List automations

Lists the automations on the profiles your key can reach, newest first, across every kind: ad rules, event automations and scheduled automations. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | Option<**String**> | Only automations on this account: the ads connection of an ad rule, or one of the `accountIds` of an event or scheduled automation. |  |
**ad_account_id** | Option<**String**> | Only ad rules checking this platform ad account. |  |
**limit** | Option<**i32**> |  |  |[default to 50]
**cursor** | Option<**String**> | `nextCursor` from the previous page. |  |

### Return type

[**models::ListAutomations200Response**](listAutomations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## pause_automation

> models::CreateAutomation201Response pause_automation(automation_id)
Turn an automation off

Pausing never needs ads access.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**automation_id** | **String** |  | [required] |

### Return type

[**models::CreateAutomation201Response**](createAutomation_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## preview_automation

> models::AutomationPreview preview_automation(automation_id, limit)
Preview a saved automation

Shows what an ad rule would do if it ran now. Nothing is changed. Event and scheduled automations cannot be previewed yet (400, `not_supported`). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**automation_id** | **String** |  | [required] |
**limit** | Option<**i32**> | How many subjects to list, matches first. `evaluated` and `matched` always count them all. |  |[default to 100]

### Return type

[**models::AutomationPreview**](AutomationPreview.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## preview_automation_draft

> models::AutomationPreview preview_automation_draft(automation_definition, limit)
Preview an unsaved automation

Shows what an ad rule would do if it ran now, without saving it or changing anything: every object it checks, each condition with its actual value, and the steps a match would run. It refuses what saving would refuse.  Event and scheduled automations cannot be previewed yet (400, `not_supported`). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**automation_definition** | [**AutomationDefinition**](AutomationDefinition.md) |  | [required] |
**limit** | Option<**i32**> | How many subjects to list, matches first. `evaluated` and `matched` always count them all. |  |[default to 100]

### Return type

[**models::AutomationPreview**](AutomationPreview.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reject_automation_approval

> models::GetAutomationApproval200Response reject_automation_approval(automation_id, approval_id, automation_approval_decision)
Reject an approval request

Rejects a pending request: every change it holds is skipped and nothing is changed on the ad account.  Only the approvers the automation names now can decide, matched by the email of the user behind the API key. Rejecting needs no ads access, like pausing. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**automation_id** | **String** |  | [required] |
**approval_id** | **String** |  | [required] |
**automation_approval_decision** | Option<[**AutomationApprovalDecision**](AutomationApprovalDecision.md)> |  |  |

### Return type

[**models::GetAutomationApproval200Response**](getAutomationApproval_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_automation

> models::CreateAutomation201Response update_automation(automation_id, update_automation_request, if_match)
Edit an automation

Replaces the top-level fields you send and keeps the rest: to change one step, send all of `steps`. The result is checked as a whole automation, so problems carry the same paths as on create.  An automation keeps its kind, and an ad rule stays on its ad account. Send `alert: null` to remove an ad rule's alert.  Send the `version` you read as `If-Match`: if the automation was saved since, the edit is refused with a 409 (`automation_stale`). An edit is also refused with a 409 when another save lands while it is being applied. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**automation_id** | **String** |  | [required] |
**update_automation_request** | [**UpdateAutomationRequest**](UpdateAutomationRequest.md) |  | [required] |
**if_match** | Option<**String**> | The automation's `version` when you read it. |  |

### Return type

[**models::CreateAutomation201Response**](createAutomation_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_automation_ad_account_controls

> models::GetAutomationControls200Response update_automation_ad_account_controls(update_automation_ad_account_controls_request)
Update one ad account's controls

Turns ad rules off or on for one ad account, sets its daily raise limit, or both. Send at least one of `paused` and `dailyRaiseLimit`; fields you leave out keep their value.  The ad account must be one the connection in `accountId` reaches, as for an automation on it. Controls apply to every ad rule of the team on that ad account. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**update_automation_ad_account_controls_request** | [**UpdateAutomationAdAccountControlsRequest**](UpdateAutomationAdAccountControlsRequest.md) |  | [required] |

### Return type

[**models::GetAutomationControls200Response**](getAutomationControls_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_automation_controls

> models::GetAutomationControls200Response update_automation_controls(update_automation_controls_request)
Turn every ad automation off or on

Turns every ad rule of the team off (`paused: true`) or back on. Each rule keeps its own status, so turning the switch back on resumes exactly the rules that were active.  Scheduled automations that boost posts are not stopped by it: pause them one by one.  It reaches every profile, so only the account owner or a full-access team member can use it. A key limited to some profiles gets 403.  Turning off a switch that is already off keeps its original `pausedAt`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**update_automation_controls_request** | [**UpdateAutomationControlsRequest**](UpdateAutomationControlsRequest.md) |  | [required] |

### Return type

[**models::GetAutomationControls200Response**](getAutomationControls_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_automation_template

> models::CreateAutomationTemplate201Response update_automation_template(template_id, update_automation_template_request)
Update an automation template

Renames a template, turns its share link on or off, or replaces its automations. Send at least one field.  Renaming or sharing keeps the `version`. New content (`from` or `automations`) is a new version; automations already installed keep the version they came from.  `visibility: link` turns the share link on (the same link while it stays on) and `visibility: team` revokes it. To copy a shared template, use `POST /v1/automations/templates` instead. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**template_id** | **String** | The template's id. | [required] |
**update_automation_template_request** | [**UpdateAutomationTemplateRequest**](UpdateAutomationTemplateRequest.md) |  | [required] |

### Return type

[**models::CreateAutomationTemplate201Response**](createAutomationTemplate_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

