# DmButton

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **Type** |  (enum: url, postback, phone) | 
**title** | **String** | Button label (20 chars max) | 
**url** | Option<**String**> | Target URL (required when type is url) | [optional]
**payload** | Option<**String**> | Postback payload delivered via the messaging_postbacks webhook (required when type is postback) | [optional]
**phone** | Option<**String**> | Phone number, e.g. +14155551234 (required when type is phone; Facebook only) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


