# AutomationTemplateAutomation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **String** | Stable within the template, for example `automation1`. | 
**definition** | **std::collections::HashMap<String, serde_json::Value>** | A `POST /v1/automations` body without `status`, in which every value tied to one account is an input reference such as `{ \"$input\": \"adAccount\" }`. Campaign ids, id filters, start and end dates and approval steps are not kept. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


