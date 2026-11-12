# CancelCommerceOrderRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Connected store SocialAccount id. | 
**reason** | **Reason** |  (enum: customer, declined, fraud, inventory, staff, other) | 
**refund** | Option<**bool**> | Refund the payments to the original methods. Authorized payments are voided either way. | [optional][default to true]
**restock** | Option<**bool**> |  | [optional][default to true]
**notify_customer** | Option<**bool**> |  | [optional][default to false]
**staff_note** | Option<**String**> | Visible to staff only. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


