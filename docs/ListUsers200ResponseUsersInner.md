# ListUsers200ResponseUsersInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**email** | Option<**String**> |  | [optional]
**role** | Option<**String**> |  | [optional]
**is_root** | Option<**bool**> |  | [optional]
**profile_access** | Option<**Vec<String>**> |  | [optional]
**created_at** | Option<**String**> |  | [optional]
**last_login_at** | Option<**String**> | Last sign-in, stamped at most once an hour, so it is accurate to within an hour rather than to the exact session. Omitted for members with no recorded sign-in since the field shipped, which does not mean they never signed in. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


