# ConnectHandoffError

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | Option<**String**> | The `error` code the flow ended on, as on a redirect_url. `connect_incomplete` when the phone reported no outcome, `connect_unverified` when it reported an account Zernio could not match to this connect. | [optional]
**message** | Option<**String**> |  | [optional]
**details** | Option<**std::collections::HashMap<String, String>**> | The other params the redirect flow appends for that error, such as `is_user_fixable`, `reason`, `dashboard_url`, `request_id` and `stage`. All optional. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


