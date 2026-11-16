# UpdateProfileRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | Option<**String**> |  | [optional]
**description** | Option<**String**> | Set to null to clear the description. | [optional]
**color** | Option<**String**> |  | [optional]
**timezone** | Option<**String**> | IANA timezone new posts on this profile use when they name no `timezone`. Set to null to go back to UTC. An unknown name returns 400. | [optional]
**external_id** | Option<**String**> | Your own identifier for this profile (1 to 255 characters, trimmed). Set to null to clear it. A value another profile of the same owner already holds returns 409 profile_external_id_conflict. | [optional]
**is_default** | Option<**bool**> |  | [optional]
**content_retention** | Option<**ContentRetention**> | Turns zero content retention on (`none`) or off (`standard`) for this profile only, for new data within about a minute. Only the team owner can change it. `standard` answers 409 while the whole team has it on; `none` answers 409 during a WhatsApp verification of a number of this profile. (enum: standard, none) | [optional]
**max_outbound_calls_per_hour** | Option<**i32**> | Caps outbound calls from this profile's numbers per rolling hour, inside the team limits. Null clears it. | [optional]
**max_daily_call_spend_usd** | Option<**f64**> | Caps billed call spend (USD) from this profile's numbers per rolling 24 hours, inside the team limits. Null clears it. | [optional]
**max_forwarded_minutes_per_day** | Option<**i32**> | Caps minutes forwarded to a phone from this profile's numbers per rolling 24 hours, inside the team limits. Null clears it. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


