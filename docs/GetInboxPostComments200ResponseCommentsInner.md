# GetInboxPostComments200ResponseCommentsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**message** | Option<**String**> |  | [optional]
**created_time** | Option<**String**> |  | [optional]
**from** | Option<[**models::GetInboxPostComments200ResponseCommentsInnerFrom**](GetInboxPostComments200ResponseCommentsInnerFrom.md)> |  | [optional]
**like_count** | Option<**i32**> |  | [optional]
**reply_count** | Option<**i32**> |  | [optional]
**platform** | Option<**String**> | The platform this comment is from | [optional]
**url** | Option<**String**> | Direct link to the comment on the platform (if available) | [optional]
**replies** | Option<**Vec<serde_json::Value>**> |  | [optional]
**can_reply** | Option<**bool**> |  | [optional]
**can_delete** | Option<**bool**> |  | [optional]
**can_hide** | Option<**bool**> | Whether this comment can be hidden (Facebook, Instagram, Threads) | [optional]
**can_like** | Option<**bool**> | Whether this comment can be liked (Facebook, Twitter/X, Bluesky, Reddit) | [optional]
**is_hidden** | Option<**bool**> | Whether the comment is currently hidden | [optional]
**is_liked** | Option<**bool**> | Whether the current user has liked this comment | [optional]
**like_uri** | Option<**String**> | Bluesky like URI for unliking | [optional]
**cid** | Option<**String**> | Bluesky content identifier | [optional]
**parent_id** | Option<**String**> | ID of the parent comment. Present on entries inside replies[] for Facebook, Instagram and X/Twitter. On X/Twitter it is also present on top-level entries, where it holds the ID of the post replied to. Omitted entirely (key absent, not null) on top-level Facebook and Instagram entries and on every other platform, which express the parent relationship only through replies[] nesting. | [optional]
**root_uri** | Option<**String**> | Bluesky root post URI | [optional]
**root_cid** | Option<**String**> | Bluesky root post CID | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


