# LookupSmsNumber200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**phone_number** | Option<**String**> |  | [optional]
**carrier_name** | Option<**String**> |  | [optional]
**line_type** | Option<**LineType**> |  (enum: mobile, landline, voip, toll-free, unknown) | [optional]
**sms_reachable** | Option<**bool**> | False for landlines, toll-free numbers, ambiguous fixed-or-mobile lines and carriers whose numbers are not SMS-routable. True is a best guess, not a delivery guarantee. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


