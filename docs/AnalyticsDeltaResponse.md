# AnalyticsDeltaResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**Vec<models::AnalyticsDeltaEntry>**](AnalyticsDeltaEntry.md) | Changed snapshots, oldest first, in the order the feed received them. Empty on the bootstrap call (no `cursor` supplied) and whenever nothing has changed since your cursor.  | 
**next_cursor** | **String** | Cursor to send on the next call. ALWAYS present, including on an empty page, so you always have something to advance with, and it never moves backwards. Opaque: pass it back verbatim, and do not parse, construct or compare cursors.  | 
**has_more** | **bool** | True when more changes are already waiting past `nextCursor`, so call again immediately. False means you are caught up: keep `nextCursor` and poll again later. This feed never ends, so `hasMore: false` does NOT mean `nextCursor` is null.  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


