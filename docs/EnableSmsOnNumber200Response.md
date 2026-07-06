# EnableSmsOnNumber200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | Option<**bool**> |  | [optional]
**id** | Option<**String**> | The SMS social account ID (present when enabled). | [optional]
**phone_number** | Option<**String**> |  | [optional]
**is_active** | Option<**bool**> | False for US numbers until their registration is approved. | [optional]
**country** | Option<**String**> |  | [optional]
**sms_capable** | Option<**bool**> | Null when capability can't be read yet (still provisioning). | [optional]
**mms_capable** | Option<**bool**> |  | [optional]
**domestic_only** | Option<**bool**> |  | [optional]
**not_ready** | Option<**bool**> | Number is still provisioning at the carrier; retry shortly. | [optional]
**needs_registration** | Option<**bool**> | US only; a carrier registration is required before delivery. | [optional]
**already_registered** | Option<**bool**> | A prior non-rejected registration already covers this number; no re-submit needed. | [optional]
**registration_status** | Option<**RegistrationStatus**> |  (enum: pending, approved, rejected, ) | [optional]
**reusable** | Option<[**models::EnableSmsOnNumber200ResponseReusable**](EnableSmsOnNumber200ResponseReusable.md)> |  | [optional]
**message** | Option<**String**> | Human-readable explanation when `enabled` is false. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


