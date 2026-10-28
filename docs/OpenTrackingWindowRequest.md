# OpenTrackingWindowRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**post_id** | Option<**String**> | Id of an external post. Required unless `accountId` and `url` are both sent. | [optional]
**account_id** | Option<**String**> | Connected account the post belongs to. Send together with `url`. | [optional]
**url** | Option<**String**> | Public URL of the post on the platform. Send together with `accountId`. | [optional]
**tracking_days** | Option<**i32**> | How many days the window stays open. | [optional][default to 30]
**requested_by** | Option<**String**> | Free-form label for who asked for the window. It is stored and returned as given. | [optional][default to api]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


