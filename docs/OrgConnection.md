# OrgConnection

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**provider** | Option<**Provider**> |  (enum: google, microsoft) | [optional]
**status** | Option<**Status**> |  (enum: pending, active, revoked) | [optional]
**profile_id** | Option<**String**> |  | [optional]
**areas** | Option<**Vec<Areas>**> |  (enum: email, calendar, files, contacts) | [optional]
**domain** | Option<**String**> |  | [optional]
**tenant_id** | Option<**String**> |  | [optional]
**admin_email** | Option<**String**> |  | [optional]
**allowed_emails** | Option<**Vec<String>**> |  | [optional]
**last_error** | Option<**String**> |  | [optional]
**verified_at** | Option<**String**> |  | [optional]
**created_at** | Option<**String**> |  | [optional]
**setup** | Option<[**models::OrgConnectionSetup**](OrgConnectionSetup.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


