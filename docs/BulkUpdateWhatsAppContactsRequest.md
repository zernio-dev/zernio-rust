# BulkUpdateWhatsAppContactsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**action** | **Action** | Bulk action to perform (enum: addTags, removeTags, addGroups, removeGroups, optIn, optOut, block, unblock) | 
**contact_ids** | **Vec<String>** | Contact IDs to update (max 500) | 
**tags** | Option<**Vec<String>**> | Tags to add or remove (required for addTags/removeTags) | [optional]
**groups** | Option<**Vec<String>**> | Groups to add or remove (required for addGroups/removeGroups) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


