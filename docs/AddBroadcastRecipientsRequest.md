# AddBroadcastRecipientsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**contact_ids** | Option<**Vec<String>**> | Specific contact IDs to add. Zernio contact ids (24-character hex), as returned by the list-contacts endpoint. A platform identifier such as a WhatsApp wa_id is rejected with 400; use phones for raw numbers. | [optional]
**phones** | Option<**Vec<String>**> | Raw phone numbers (auto-creates contacts). Useful for WhatsApp/Telegram manual entry | [optional]
**use_segment** | Option<**bool**> | Auto-populate from broadcast segment filters | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


