# TrackingTag

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Platform-native tag id. Meta: numeric pixel id, as a string. | 
**name** | **String** |  | 
**platform** | **Platform** |  (enum: metaads) | 
**kind** | **Kind** | Platform-native flavor of the tag (Meta: `pixel`). (enum: pixel, tag, insight_tag) | 
**status** | **Status** | `inactive` when the platform reports the tag as broken/unavailable. (enum: active, inactive) | 
**code** | Option<**String**> | The base-code `<script>` snippet to install on the site. Meta only; populated by `getTrackingTag`, omitted from the list view.  | [optional]
**last_fired_time** | Option<**i32**> | Unix seconds of the last event the tag received, or `null` if it never fired. The practical \"is it installed and working\" signal.  | [optional]
**is_unavailable** | Option<**bool**> | Whether the tag is in a broken/unavailable state (Meta `is_unavailable`). | [optional]
**installed** | Option<**bool**> | Convenience flag derived from `lastFiredTime` — has the tag ever fired. | [optional]
**creation_time** | Option<**i32**> | Unix seconds the tag was created. | [optional]
**owner_business_id** | Option<**String**> | Business Manager id that owns the tag, or `null` when the tag lives on a personal (non-BM) ad account — such tags can't be shared with other ad accounts.  | [optional]
**owner_ad_account_id** | Option<**String**> | Ad account id (`act_...`) that owns the tag, when reported. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


