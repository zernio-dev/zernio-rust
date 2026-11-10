# Profile

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | Option<**String**> |  | [optional]
**user_id** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**description** | Option<**String**> |  | [optional]
**color** | Option<**String**> |  | [optional]
**timezone** | Option<**String**> | IANA timezone new posts on this profile use when the request names no `timezone`. Null means UTC. | [optional]
**external_id** | Option<**String**> | Your own identifier for this profile, set on create or update. Null when none is set. | [optional]
**content_retention** | Option<**ContentRetention**> | This profile's own zero content retention setting. `none` stores identifiers and metadata only for this profile. Change it with `contentRetention` on update; only the team owner can. (enum: standard, none) | [optional]
**effective_content_retention** | Option<**EffectiveContentRetention**> | The mode that applies to this profile: `none` when the profile or the whole team uses zero content retention. (enum: standard, none) | [optional]
**is_default** | Option<**bool**> |  | [optional]
**is_over_limit** | Option<**bool**> | Only present when includeOverLimit=true. Indicates if this profile exceeds the plan limit. | [optional]
**account_count** | Option<**i32**> | In the profile list. Connected accounts on the profile, including ones that need reconnecting; phone and SMS number internals and posting accounts hidden by an ads connect are not counted. | [optional]
**created_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


