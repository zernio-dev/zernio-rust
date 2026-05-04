# UpdateAccountRequestXCapabilities

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**analytics** | Option<**bool**> | Enable periodic analytics reads (impressions, likes, etc.) for this X account. Each X API call is metered as `posts_read` and billed pass-through (~$0.005/call at the time of writing — actual rate depends on X's pricing tier).  | [optional]
**inbox** | Option<**bool**> | Enable DM polling and inbox sync for this X account. DM reads are metered as `dm_event_read` (~$0.010/call) and DM sends as `dm_interaction_create` (~$0.015/call), both billed pass-through. DM sends fire only on user-initiated actions; reads/polling fire only when this flag is true.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


