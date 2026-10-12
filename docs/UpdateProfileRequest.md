# UpdateProfileRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | Option<**String**> |  | [optional]
**description** | Option<**String**> | Set to null to clear the description. | [optional]
**color** | Option<**String**> |  | [optional]
**timezone** | Option<**String**> | IANA timezone new posts on this profile use when they name no `timezone`. Set to null to go back to UTC. An unknown name returns 400. | [optional]
**external_id** | Option<**String**> | Your own identifier for this profile (1 to 255 characters, trimmed). Set to null to clear it. A value another profile of the same owner already holds returns 409 profile_external_id_conflict. | [optional]
**is_default** | Option<**bool**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


