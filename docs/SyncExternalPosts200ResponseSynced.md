# SyncExternalPosts200ResponseSynced

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**posts_found** | Option<**i32**> | Posts returned by the platform listing during the on-demand sync | [optional]
**posts_synced** | Option<**i32**> | Posts inserted or updated in Zernio | [optional]
**skipped** | Option<**bool**> | True when no live fetch ran: the post was already stored, or the account was synced within the debounce window | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


