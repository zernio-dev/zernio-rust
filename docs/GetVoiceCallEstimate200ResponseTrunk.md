# GetVoiceCallEstimate200ResponseTrunk

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Trunk the limits were read from. Null when none was resolved and the defaults apply. | [optional]
**limits_source** | Option<**LimitsSource**> |  (enum: trunk, default) | [optional]
**max_destination_rate_usd** | Option<**f64**> | Per-minute cap, compared with the carrier's rate for the route (half the billed rate). Default 0.30, null when the trunk has no cap. | [optional]
**destination_whitelisted** | Option<**bool**> | Whether destinationCountry is on the trunk's whitelist. The default whitelist is every country Zernio sells numbers in. | [optional]
**rate_check** | Option<**RateCheck**> | `partial` means some of the destination's networks are above the cap and calls to them are refused. (enum: under, partial, over) | [optional]
**outbound_enabled** | Option<**bool**> | False while outbound is paused for an unfunded balance. Null with default limits. | [optional]
**would_block** | Option<**bool**> |  | [optional]
**block_reasons** | Option<**Vec<BlockReasons>**> |  (enum: destination_not_whitelisted, rate_above_cap, outbound_paused) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


