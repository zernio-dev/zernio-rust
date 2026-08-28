# GetYoutubeCaptions200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | Option<**String**> |  | [optional]
**video_id** | Option<**String**> |  | [optional]
**language** | Option<**String**> | The language of the returned track. | [optional]
**track_id** | Option<**String**> | YouTube's own caption track id. | [optional]
**track_kind** | Option<**TrackKind**> | `asr` is YouTube's auto-generated track; `standard` was uploaded by the channel. (enum: asr, standard) | [optional]
**source** | Option<**Source**> | `cache` when served from our stored copy, `youtube` when this call spent the quota units. (enum: cache, youtube) | [optional]
**fetched_at** | Option<**String**> | When the stored copy was downloaded from YouTube. | [optional]
**text** | Option<**String**> | The whole transcript as one paragraph, no timings. | [optional]
**cues** | Option<[**Vec<models::GetYoutubeCaptions200ResponseCuesInner>**](GetYoutubeCaptions200ResponseCuesInner.md)> | Timed cues. Present when format is json. Auto-generated cues overlap in time by design (captions roll), so `start` can precede the previous cue's `end`. | [optional]
**srt** | Option<**String**> | Raw SubRip body. Present when format is srt. | [optional]
**available_tracks** | Option<[**Vec<models::GetYoutubeCaptions200ResponseAvailableTracksInner>**](GetYoutubeCaptions200ResponseAvailableTracksInner.md)> | Every track on the video, so you can re-request another language. On a cached read this is the listing as it stood when we downloaded, so a language added to the video since then appears only after a `refresh=true` or when you request that language directly. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


