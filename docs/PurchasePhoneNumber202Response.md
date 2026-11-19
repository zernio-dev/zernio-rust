# PurchasePhoneNumber202Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | Option<**Status**> |  (enum: kyc_required) | [optional]
**country** | Option<**String**> |  | [optional]
**number_type** | Option<**String**> | The type that will be ordered after KYC approval. | [optional]
**purchase_intent_id** | Option<**String**> | Echo of the purchaseIntentId you sent. Pass it to the KYC submission (or the KYC share link) so the resulting numbers and their whatsapp.number.* webhooks carry it. | [optional]
**kyc_url** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


