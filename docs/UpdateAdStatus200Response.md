# UpdateAdStatus200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**updated** | Option<**i32**> | 1 when the switch was written, 0 when skipped | [optional]
**skipped** | Option<**i32**> | 1 when skipped (terminal status, or the ad's own switch already in the target state), else 0 | [optional]
**status** | Option<**String**> | The ad's delivery status after the call, as the platform reports it when it can be read back (e.g. `paused` for an ad switched on under a paused campaign) | [optional]
**configured_status** | Option<**String**> | The ad's own on/off switch (`ACTIVE` / `PAUSED`), re-read from the platform after the write. Null where the platform exposes no per-ad switch (X) or the read-back failed and the platform does not store one. | [optional]
**message** | Option<**String**> | Human-readable summary (present only when skipped), e.g. \"No change: the ad's own switch is already off\" | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


