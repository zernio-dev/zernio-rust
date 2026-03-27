# WebhookPayloadAccountDisconnectedAccount

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | The account's unique identifier (same as used in /v1/accounts/{accountId}) | 
**profile_id** | **String** | The profile's unique identifier this account belongs to | 
**platform** | **String** |  | 
**username** | **String** |  | 
**display_name** | Option<**String**> |  | [optional]
**disconnection_type** | **DisconnectionType** | Whether the disconnection was intentional (user action) or unintentional (token expired/revoked) (enum: intentional, unintentional) | 
**reason** | **String** | Human-readable reason for the disconnection | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


