# \CommentsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_inbox_comment**](CommentsApi.md#delete_inbox_comment) | **DELETE** /v1/inbox/comments/{postId} | Delete comment
[**edit_inbox_comment**](CommentsApi.md#edit_inbox_comment) | **PATCH** /v1/inbox/comments/{postId}/{commentId} | Edit comment
[**get_inbox_post_comments**](CommentsApi.md#get_inbox_post_comments) | **GET** /v1/inbox/comments/{postId} | Get post comments
[**hide_inbox_comment**](CommentsApi.md#hide_inbox_comment) | **POST** /v1/inbox/comments/{postId}/{commentId}/hide | Hide comment
[**like_inbox_comment**](CommentsApi.md#like_inbox_comment) | **POST** /v1/inbox/comments/{postId}/{commentId}/like | Like comment
[**list_inbox_comments**](CommentsApi.md#list_inbox_comments) | **GET** /v1/inbox/comments | List commented posts
[**reply_to_inbox_post**](CommentsApi.md#reply_to_inbox_post) | **POST** /v1/inbox/comments/{postId} | Reply to comment
[**send_private_reply_to_comment**](CommentsApi.md#send_private_reply_to_comment) | **POST** /v1/inbox/comments/{postId}/{commentId}/private-reply | Send private reply
[**set_comment_moderation**](CommentsApi.md#set_comment_moderation) | **POST** /v1/inbox/comments/{postId}/{commentId}/moderation | Set comment moderation status
[**unhide_inbox_comment**](CommentsApi.md#unhide_inbox_comment) | **DELETE** /v1/inbox/comments/{postId}/{commentId}/hide | Unhide comment
[**unlike_inbox_comment**](CommentsApi.md#unlike_inbox_comment) | **DELETE** /v1/inbox/comments/{postId}/{commentId}/like | Unlike comment



## delete_inbox_comment

> models::DeleteInboxComment200Response delete_inbox_comment(post_id, account_id, comment_id)
Delete comment

Delete a comment on a post. Supported by Facebook, Instagram, Bluesky, Reddit, YouTube, and LinkedIn. Requires accountId and commentId query parameters. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** | Zernio post ID or platform-specific post ID. LinkedIn third-party posts accept full activity URN or numeric ID. | [required] |
**account_id** | **String** |  | [required] |
**comment_id** | **String** |  | [required] |

### Return type

[**models::DeleteInboxComment200Response**](deleteInboxComment_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## edit_inbox_comment

> models::EditInboxComment200Response edit_inbox_comment(post_id, comment_id, edit_inbox_comment_request)
Edit comment

Edit the body of a comment the connected account posted. Supported on Reddit only.  Reddit keeps the same comment id after an edit. Reddit exposes no API to edit a post title, and a link post has no editable body. To edit a published post's body, use `POST /v1/posts/{postId}/edit`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** |  | [required] |
**comment_id** | **String** |  | [required] |
**edit_inbox_comment_request** | [**EditInboxCommentRequest**](EditInboxCommentRequest.md) |  | [required] |

### Return type

[**models::EditInboxComment200Response**](editInboxComment_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_inbox_post_comments

> models::GetInboxPostComments200Response get_inbox_post_comments(post_id, account_id, subreddit, limit, cursor, comment_id)
Get post comments

Fetch comments for a specific post. Requires accountId query parameter.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** | Zernio post ID or platform-specific post ID. Zernio IDs are auto-resolved. LinkedIn third-party posts accept full activity URN or numeric ID. | [required] |
**account_id** | **String** |  | [required] |
**subreddit** | Option<**String**> | (Reddit only) Subreddit name |  |
**limit** | Option<**i32**> | Maximum number of comments to return |  |[default to 25]
**cursor** | Option<**String**> | Pagination cursor |  |
**comment_id** | Option<**String**> | (Reddit only) Get replies to a specific comment |  |

### Return type

[**models::GetInboxPostComments200Response**](getInboxPostComments_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## hide_inbox_comment

> models::HideInboxComment200Response hide_inbox_comment(post_id, comment_id, hide_inbox_comment_request)
Hide comment

Hide a comment on a post. Supported by Facebook, Instagram, Threads, and X/Twitter. Hidden comments are only visible to the commenter and page admin. For X/Twitter, the reply must belong to a conversation started by the authenticated user. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** |  | [required] |
**comment_id** | **String** |  | [required] |
**hide_inbox_comment_request** | [**HideInboxCommentRequest**](HideInboxCommentRequest.md) |  | [required] |

### Return type

[**models::HideInboxComment200Response**](hideInboxComment_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## like_inbox_comment

> models::LikeInboxComment200Response like_inbox_comment(post_id, comment_id, like_inbox_comment_request)
Like comment

Like or upvote a comment on a post. Supported platforms: Facebook, Twitter/X, Bluesky, Reddit. For Bluesky, the cid (content identifier) is required in the request body. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** |  | [required] |
**comment_id** | **String** |  | [required] |
**like_inbox_comment_request** | [**LikeInboxCommentRequest**](LikeInboxCommentRequest.md) |  | [required] |

### Return type

[**models::LikeInboxComment200Response**](likeInboxComment_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_inbox_comments

> models::ListInboxComments200Response list_inbox_comments(profile_id, platform, min_comments, since, sort_by, sort_order, limit, cursor, account_id)
List commented posts

Returns posts with comment counts from all connected accounts. Aggregates data across multiple accounts.  For users with the Ads add-on (Metronome plans always qualify), the user's Meta ads (boosted/dark posts) are included too. There's one row per (ad, placement-with-comments): an ad that runs on both Facebook feed and Instagram feed produces up to two rows (the Page dark post and the IG media have separate comment threads), each flagged `isAd: true` with `adId` and `placement` (`id` is `{adId}:{placement}`). Use `?platform=metaads` to return *only* ad rows; passing `facebook`/`instagram` returns *organic* posts only (no ads); omitting `platform` returns both. Fetch a row's thread from GET /v1/ads/{adId}/comments?placement={placement}. Ad comment counts are read with the Marketing API token (Facebook side) or the connected Instagram account's token (Instagram side); a row whose count can't be read is omitted. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | Option<**String**> | Filter by profile ID |  |
**platform** | Option<**String**> | Filter by platform. `metaads` is a synthetic value meaning the user's ads (boosted/dark posts) only; `facebook`/`instagram` return organic posts only. |  |
**min_comments** | Option<**i32**> | Minimum comment count |  |
**since** | Option<**String**> | Posts created after this date |  |
**sort_by** | Option<**String**> | Sort field |  |[default to date]
**sort_order** | Option<**String**> | Sort order |  |[default to desc]
**limit** | Option<**i32**> |  |  |[default to 50]
**cursor** | Option<**String**> |  |  |
**account_id** | Option<**String**> | Filter by specific social account ID |  |

### Return type

[**models::ListInboxComments200Response**](listInboxComments_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reply_to_inbox_post

> models::ReplyToInboxPost200Response reply_to_inbox_post(post_id, reply_to_inbox_post_request)
Reply to comment

Post a reply to a post or specific comment. Requires accountId in request body.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** | Zernio post ID or platform-specific post ID. LinkedIn third-party posts accept full activity URN or numeric ID. | [required] |
**reply_to_inbox_post_request** | [**ReplyToInboxPostRequest**](ReplyToInboxPostRequest.md) |  | [required] |

### Return type

[**models::ReplyToInboxPost200Response**](replyToInboxPost_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## send_private_reply_to_comment

> models::SendPrivateReplyToComment200Response send_private_reply_to_comment(post_id, comment_id, send_private_reply_to_comment_request)
Send private reply

Send a private message to the author of a comment. Supported on Instagram and Facebook only. One reply per comment, must be sent within 7 days. Optionally attach interactive elements: `quickReplies` (chips above the keyboard, max 13) or `buttons` (1-3 inline postback/url buttons rendered in the same bubble via Meta's button_template). Buttons are recommended for cold reach since chips do not render in the Instagram Message Requests folder. `quickReplies` and `buttons` are mutually exclusive. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** | The media/post ID (Instagram media ID or Facebook post ID) | [required] |
**comment_id** | **String** | The comment ID to send a private reply to | [required] |
**send_private_reply_to_comment_request** | [**SendPrivateReplyToCommentRequest**](SendPrivateReplyToCommentRequest.md) |  | [required] |

### Return type

[**models::SendPrivateReplyToComment200Response**](sendPrivateReplyToComment_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## set_comment_moderation

> models::UpdateYoutubeDefaultPlaylist200Response set_comment_moderation(post_id, comment_id, set_comment_moderation_request)
Set comment moderation status

Set a comment's moderation status. Supported on YouTube only.  Use this to work a moderation queue: approve a held comment (`published`), reject it (`rejected`), or send it back for review (`heldForReview`).  The request must be authorized by the owner of the channel or video the comment belongs to. You cannot moderate comments on videos you do not own.  This is distinct from `POST /v1/inbox/comments/{postId}/{commentId}/hide`, which covers Facebook, Instagram, Threads, and X/Twitter and does not apply to YouTube. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** |  | [required] |
**comment_id** | **String** |  | [required] |
**set_comment_moderation_request** | [**SetCommentModerationRequest**](SetCommentModerationRequest.md) |  | [required] |

### Return type

[**models::UpdateYoutubeDefaultPlaylist200Response**](updateYoutubeDefaultPlaylist_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## unhide_inbox_comment

> models::HideInboxComment200Response unhide_inbox_comment(post_id, comment_id, account_id)
Unhide comment

Unhide a previously hidden comment. Supported by Facebook, Instagram, Threads, and X/Twitter. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** |  | [required] |
**comment_id** | **String** |  | [required] |
**account_id** | **String** |  | [required] |

### Return type

[**models::HideInboxComment200Response**](hideInboxComment_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## unlike_inbox_comment

> models::UnlikeInboxComment200Response unlike_inbox_comment(post_id, comment_id, account_id, like_uri)
Unlike comment

Remove a like from a comment. Supported platforms: Facebook, Twitter/X, Bluesky, Reddit. For Bluesky, the likeUri query parameter is required. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** |  | [required] |
**comment_id** | **String** |  | [required] |
**account_id** | **String** |  | [required] |
**like_uri** | Option<**String**> | (Bluesky only) The like URI returned when liking |  |

### Return type

[**models::UnlikeInboxComment200Response**](unlikeInboxComment_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

