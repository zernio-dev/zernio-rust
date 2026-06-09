# RedditPlatformData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**subreddit** | Option<**String**> | Target subreddit name (without \"r/\" prefix). Overrides the default. Use GET /v1/accounts/{id}/reddit-subreddits to list options. | [optional]
**title** | Option<**String**> | Post title. Defaults to the first line of content, truncated to 300 characters. | [optional]
**url** | Option<**String**> | URL for link posts. If provided (and forceSelf is not true), creates a link post instead of a text post. | [optional]
**force_self** | Option<**bool**> | When true, creates a text/self post even when a URL or media is provided. | [optional]
**flair_id** | Option<**String**> | Flair ID for the post. Required by some subreddits. Use GET /v1/accounts/{id}/reddit-flairs?subreddit=name to list flairs. | [optional]
**flair_text** | Option<**String**> | Custom flair text, for subreddits that allow free-text flair. Ignored when flairId is provided (flairId wins). | [optional]
**nsfw** | Option<**bool**> | Mark the post as NSFW (Not Safe For Work / over 18). | [optional][default to false]
**spoiler** | Option<**bool**> | Mark the post as a spoiler. The subreddit must have spoiler tagging enabled for this to take effect. | [optional][default to false]
**sendreplies** | Option<**bool**> | Whether to receive inbox replies for comments on this post. Set to false to opt out. | [optional][default to true]
**native_video** | Option<**bool**> | Controls Reddit's native video upload flow. When true (default for video mediaItems), the video is uploaded to Reddit's CDN and submitted with kind=video so it renders as an embedded Reddit video player. Reddit transcodes server-side (1080p/30fps cap). Set to false to fall back to a legacy link post. If the subreddit blocks video posts, the upload falls back to a link post automatically.  | [optional][default to true]
**videogif** | Option<**bool**> | When true (and nativeVideo is active), submits the video as a silent videogif (kind=videogif). Use for short looping clips without audio. | [optional]
**video_poster_url** | Option<**String**> | Optional poster/thumbnail image URL for native video posts. If omitted, the first frame of the video is extracted and used automatically. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


