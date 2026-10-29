# CtwaSingleResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ad_type** | **AdType** |  (enum: single) | 
**ad** | **serde_json::Value** | The persisted Ad document. | 
**message** | **String** |  | 
**warnings** | Option<**Vec<String>**> | Present when Meta created the ad set differently from the request:  - Multi-destination ad set (`destinations` including whatsapp) that Meta kept without the requested `whatsappPhoneNumber` in its promoted_object, which an existing ad set cannot change. A WhatsApp-only ad set returns no such warning, because every ad routes conversations by the number on its WhatsApp button. - The ad set joined a CBO campaign (`existingCampaignId`) whose own bid strategy applies, so a different `bidStrategy` or a `roasAverageFloor` that strategy cannot take was not applied. - An entry starting with `activation_failed:`: Meta refused the final switch to ACTIVE. Nothing was deleted. The entry names what was kept PAUSED and what was switched ACTIVE, and quotes Meta's error and the status calls that switch the PAUSED ones on later.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


