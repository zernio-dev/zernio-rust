# CreateContactRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** |  | 
**name** | **String** |  | 
**email** | Option<**String**> |  | [optional]
**company** | Option<**String**> |  | [optional]
**tags** | Option<**Vec<String>**> |  | [optional]
**is_subscribed** | Option<**bool**> |  | [optional][default to true]
**notes** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> | Optional. Creates a channel if provided with platform + platformIdentifier | [optional]
**platform** | Option<**Platform**> | Channel platform. Only the enum values support contact channels; any other platform is rejected with code platform_not_supported. (enum: instagram, facebook, telegram, twitter, bluesky, reddit, whatsapp, slack) | [optional]
**platform_identifier** | Option<**String**> |  | [optional]
**display_identifier** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


