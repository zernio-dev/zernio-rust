# PinterestPlatformData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | Option<**String**> | Pin title. Defaults to first line of content or \"Pin\". Must be ≤ 100 characters. | [optional]
**board_id** | Option<**String**> | Target Pinterest board ID. If omitted, the first available board is used. | [optional]
**board_section_id** | Option<**String**> | Target section inside the board. Optional; the pin lands on the board itself when omitted. Pinterest rejects the pin if the section does not belong to boardId, so send both together. | [optional]
**link** | Option<**String**> | Destination link (pin URL) | [optional]
**cover_image_url** | Option<**String**> | Optional cover image for video pins | [optional]
**cover_image_key_frame_time** | Option<**i32**> | Optional key frame time in seconds for derived video cover | [optional]
**is_ai_generated** | Option<**bool**> | When true, the Pin is created with Pinterest's AI_MODIFIED disclosure (ai_disclosures), which shows an \"AI modified\" label. Applies to image and video Pins. Pinterest offers no \"not AI\" value, so false simply omits the disclosure. Pinterest may still label a Pin on its own detection. | [optional][default to false]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


