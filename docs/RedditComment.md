# RedditComment

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Reddit comment ID (without type prefix) | [optional]
**fullname** | Option<**String**> | Reddit fullname (e.g. t1_abc123) | [optional]
**parent_id** | Option<**String**> | Fullname of what the comment answers: the post (t3_…) or a parent comment (t1_…) | [optional]
**author** | Option<**String**> | The username, or [deleted] | [optional]
**body** | Option<**String**> | Comment text as written (Markdown, not HTML-escaped), or [deleted] / [removed] | [optional]
**permalink** | Option<**String**> | Full permalink to the comment | [optional]
**created_utc** | Option<**f64**> | Unix timestamp of the comment | [optional]
**score** | Option<**i32**> |  | [optional]
**num_replies** | Option<**i32**> | Direct replies included in this response; replies Reddit left out are listed in more | [optional]
**depth** | Option<**i32**> | 0 for a top-level comment of this response, 1 for a reply to it, and so on | [optional]
**is_submitter** | Option<**bool**> | Whether the author is the post's author | [optional]
**edited** | Option<**bool**> |  | [optional]
**stickied** | Option<**bool**> |  | [optional]
**distinguished** | Option<**String**> | \"moderator\" or \"admin\" when the comment is distinguished, else null | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


