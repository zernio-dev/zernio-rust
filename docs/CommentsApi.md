# \CommentsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_inbox_comment**](CommentsApi.md#delete_inbox_comment) | **DELETE** /v1/inbox/comments/{postId} | Delete comment
[**edit_inbox_comment**](CommentsApi.md#edit_inbox_comment) | **PATCH** /v1/inbox/comments/{postId}/{commentId} | Edit comment
[**get_inbox_post_comments**](CommentsApi.md#get_inbox_post_comments) | **GET** /v1/inbox/comments/{postId} | Get post comments
[**hide_inbox_comment**](CommentsApi.md#hide_inbox_comment) | **POST** /v1/inbox/comments/{postId}/{commentId}/hide | Hide comment
[**like_inbox_comment**](CommentsApi.md#like_inbox_comment) | **POST** /v1/inbox/comments/{postId}/{commentId}/like | Like comment
[**like_post**](CommentsApi.md#like_post) | **POST** /v1/inbox/posts/{postId}/like | Like post
[**list_inbox_comments**](CommentsApi.md#list_inbox_comments) | **GET** /v1/inbox/comments | List commented posts
[**reply_to_inbox_post**](CommentsApi.md#reply_to_inbox_post) | **POST** /v1/inbox/comments/{postId} | Reply to comment
[**send_private_reply_to_comment**](CommentsApi.md#send_private_reply_to_comment) | **POST** /v1/inbox/comments/{postId}/{commentId}/private-reply | Send private reply
[**set_comment_moderation**](CommentsApi.md#set_comment_moderation) | **POST** /v1/inbox/comments/{postId}/{commentId}/moderation | Set comment moderation status
[**unhide_inbox_comment**](CommentsApi.md#unhide_inbox_comment) | **DELETE** /v1/inbox/comments/{postId}/{commentId}/hide | Unhide comment
[**unlike_inbox_comment**](CommentsApi.md#unlike_inbox_comment) | **DELETE** /v1/inbox/comments/{postId}/{commentId}/like | Unlike comment
[**unlike_post**](CommentsApi.md#unlike_post) | **DELETE** /v1/inbox/posts/{postId}/like | Unlike post



## delete_inbox_comment

> models::DeleteInboxComment200Response delete_inbox_comment(post_id, account_id, comment_id)
Delete comment

Delete a comment on a post. Supported by Facebook, Instagram, Bluesky, Reddit, YouTube, and LinkedIn. Requires accountId and commentId query parameters. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** | Zernio post ID or platform-specific post ID. LinkedIn third-party posts accept full activity URN or numeric ID. | [required] |
**account_id** | **String** |  | [required] |
**comment_id** | **String** | For LinkedIn, accepts either the numeric comment ID or the composite comment URN returned by the comments listing (e.g. urn:li:comment:(threadUrn,id)) | [required] |

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

Fetch comments for a specific post. Requires accountId query parameter.  On Facebook and Instagram, passing a COMMENT id as `postId` is also supported and returns that comment's replies instead of the post's top-level comments. This is not available on YouTube, where `postId` must be a video id.  Responses are cached for up to 10 minutes, so a page may lag new comments by that window. Do not poll this endpoint for real-time updates: subscribe to the `comment.received` webhook, which delivers new comments as they arrive. Your own writes (creating, replying to, or deleting a comment) refresh the cache immediately. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** | Zernio post ID or platform-specific post ID. Zernio IDs are auto-resolved. LinkedIn third-party posts accept full activity URN or numeric ID. On Facebook and Instagram, a comment ID is also accepted here and returns that comment's replies. | [required] |
**account_id** | **String** |  | [required] |
**subreddit** | Option<**String**> | (Reddit only) Subreddit name |  |
**limit** | Option<**i32**> | Maximum number of comments to return |  |[default to 25]
**cursor** | Option<**String**> | Pagination cursor, returned by a previous call as `pagination.cursor`. This is the platform's own opaque paging value passed through verbatim: never construct, decode or validate it client-side. |  |
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

Like or upvote a comment on a post. Supported platforms: Facebook, Twitter/X, Bluesky, Reddit, LinkedIn, and Instagram in limited release (see below). For Bluesky, the cid (content identifier) is required in the request body. For LinkedIn, pass the composite comment URN returned by the comments endpoints as commentId; an optional reactionType picks the reaction (defaults to LIKE), and accounts connected before the social-feed scopes were requested get a 403 with code `linkedin_reconnect_required`.  Instagram is in LIMITED RELEASE and not generally available: the call needs `instagram_manage_engagement`, which Meta has so far granted this app only under Standard Access, so it works for app admins, developers and testers of our Meta app and returns a 403 with code `PLATFORM_BETA_RESTRICTED` for every other account. That restriction lifts when Meta App Review grants Advanced Access; the constraints below apply once it does.  Instagram covers comments and replies on feed posts, reels and carousels. Only an account connected through Facebook Login can be granted `instagram_manage_engagement`: an Instagram Login connection returns a 400 with code `instagram_likes_require_facebook_login`, and an account whose token predates the permission returns a 403 with code `reconnect_required`. Content from private accounts cannot be liked. Instagram also enforces a burst limit of 50 like or unlike calls per 5 seconds per Instagram account, and exceeding it locks that account out of the like API for an hour, so pace bulk loops. 

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


## like_post

> models::LikePost200Response like_post(post_id, like_post_request)
Like post

Like (or react to) a post as a connected account. Supported platforms: LinkedIn, Twitter/X, Facebook, YouTube, Bluesky, and Instagram in limited release (see below). Threads, TikTok and Pinterest expose no like endpoint in their APIs and return 400. Reddit returns 400 too, pointing at `POST /v1/accounts/{accountId}/reddit-vote`, which covers upvote, downvote and clear on both posts and comments.  The account does not have to be the one that published the post, which is what makes executive engagement possible: pass an exec's `accountId` and the brand post's ID. `postId` accepts either a Zernio post ID or the platform's native post ID. A Zernio post ID resolves to the entry for `accountId`, falling back to the post's single entry on the same platform (two entries on that platform is a 400, so pass the native ID).  LinkedIn requires the `w_member_social_feed` / `w_organization_social_feed` scopes, which are not retroactive: accounts connected before those were requested get a 403 with code `linkedin_reconnect_required` until the user reconnects the account. YouTube spends 50 quota units per call.  Instagram is in LIMITED RELEASE and not generally available: the call needs `instagram_manage_engagement`, which Meta has so far granted this app only under Standard Access, so it works for app admins, developers and testers of our Meta app and returns a 403 with code `PLATFORM_BETA_RESTRICTED` for every other account. That restriction lifts when Meta App Review grants Advanced Access; the constraints below apply once it does.  Instagram covers feed images, reels and carousels (stories and private-account media are not likeable). Only an account connected through Facebook Login can be granted `instagram_manage_engagement`: an Instagram Login connection returns a 400 with code `instagram_likes_require_facebook_login`, and an account whose token predates the permission returns a 403 with code `reconnect_required`. Instagram also enforces a burst limit of 50 like or unlike calls per 5 seconds per Instagram account, and exceeding it locks that account out of the like API for an hour, so pace bulk loops. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** | Zernio post ID or the platform's native post ID | [required] |
**like_post_request** | [**LikePostRequest**](LikePostRequest.md) |  | [required] |

### Return type

[**models::LikePost200Response**](likePost_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_inbox_comments

> models::ListInboxComments200Response list_inbox_comments(profile_id, platform, min_comments, since, sort_by, sort_order, limit, cursor, account_id)
List commented posts

Returns posts with comment counts from all connected accounts. Aggregates data across multiple accounts.  Responses are cached for up to 10 minutes, so the feed may lag new comments by that window. Do not poll this endpoint for real-time updates: subscribe to the `comment.received` webhook, which fires for every new comment across your posts and carries the post reference needed to keep this list current.  For users with the Ads add-on (Metronome plans always qualify), the user's Meta ads (boosted/dark posts) are included too. There's one row per (ad, placement-with-comments): an ad that runs on both Facebook feed and Instagram feed produces up to two rows (the Page dark post and the IG media have separate comment threads), each flagged `isAd: true` with `adId` and `placement` (`id` is `{adId}:{placement}`). Use `?platform=metaads` to return *only* ad rows; passing `facebook`/`instagram` returns *organic* posts only (no ads); omitting `platform` returns both. Fetch a row's thread from GET /v1/ads/{adId}/comments?placement={placement}. Ad comment counts are read with the Marketing API token (Facebook side) or the connected Instagram account's token (Instagram side); a row whose count can't be read is omitted.  Pagination walks each account's platform listing. Following `nextCursor` reaches past the first page on Facebook, Instagram, Threads, LinkedIn and YouTube, since they are the platforms that support a server-side date window; on the others the listing stops at its first page. Cursor pagination is only coherent for the default sort (`sortBy=date`, `sortOrder=desc`): with `sortOrder=asc`, or with `sortBy=comments`, the cursor filter does not match the sort order and the second page is unreliable.  `nextCursor` is opaque: pass it back verbatim, never construct or parse it, its composition may change without notice. Because each page re-queries a live window, results can still shift between requests, so dedupe by `id` on the client.  `commentCount` semantics differ by platform: YouTube's includes replies, Facebook's counts top-level comments only. 

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

> models::ReplyToInboxPost200Response reply_to_inbox_post(post_id, reply_to_inbox_post_request, idempotency_key)
Reply to comment

Post a reply to a post or specific comment. Requires accountId in request body.  **Idempotency:** send an `Idempotency-Key` header to make retries safe (e.g. after a client-side timeout where delivery is unknown): same key + same body replays the original response (with `Idempotent-Replayed: true`) instead of posting the comment a second time; same key + different body returns 422; a key still in flight returns 409. Keys are retained for 24 hours and are scoped to the credential and to this exact path, so reusing a key against a different postId returns 422 rather than replaying the other post's response.  Only successful (2xx) responses are stored for replay. If the request throws or returns a non-2xx status the key is released, so the header protects the \"request succeeded but the response was lost\" case. After an ambiguous failure (a 5xx or a network timeout) list the post's comments before retrying with the same key, and treat an empty result as inconclusive rather than as proof nothing was posted. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** | Zernio post ID or platform-specific post ID. LinkedIn third-party posts accept full activity URN or numeric ID. | [required] |
**reply_to_inbox_post_request** | [**ReplyToInboxPostRequest**](ReplyToInboxPostRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. |  |

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

Send a private message to the author of a comment. Supported on Instagram and Facebook only. One reply per comment, must be sent within 7 days. Optionally attach interactive elements: `quickReplies` (chips above the keyboard, max 13) or `buttons` (1-3 inline postback/url buttons rendered in the same bubble via Meta's button_template). Chips do not render in the Instagram Message Requests folder. Since late August 2026 Instagram refuses buttons, cards and attachments to commenters who do not follow the account (Meta code 2, subcode 1545133, returned here as a non-retryable 400 that says so), and the failed call still consumes the comment's single private reply. To reach non-followers send plain text and add buttons once they reply. `quickReplies` and `buttons` are mutually exclusive. 

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

Remove a like from a comment. Supported platforms: Facebook, Twitter/X, Bluesky, Reddit, LinkedIn, and Instagram in limited release. For Bluesky, the likeUri query parameter is required. Instagram has the same limited release, Facebook Login, `instagram_manage_engagement` and burst-limit constraints as liking. 

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


## unlike_post

> models::UnlikePost200Response unlike_post(post_id, account_id, like_uri)
Unlike post

Remove this account's like from a post. Supported platforms: LinkedIn, Twitter/X, Facebook, YouTube, Bluesky, and Instagram in limited release. On YouTube this clears the rating. Instagram has the same limited release, Facebook Login, `instagram_manage_engagement` and burst-limit constraints as liking. For Bluesky, `likeUri` (returned when the post was liked) is required. Reddit uses `POST /v1/accounts/{accountId}/reddit-vote` with `direction: 0`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** | Zernio post ID or the platform's native post ID | [required] |
**account_id** | **String** |  | [required] |
**like_uri** | Option<**String**> | (Bluesky only) The like URI returned when liking |  |

### Return type

[**models::UnlikePost200Response**](unlikePost_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

