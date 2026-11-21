# CreateCrmActivityRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**body** | **String** | The text to log. | 
**subject** | Option<**String**> | Salesforce Task subject (default `<Channel> activity (<direction>)`); on HubSpot, the bold first line; on HighLevel, the note's first line. | [optional]
**channel** | Option<**Channel**> |  (enum: whatsapp, sms, email, call, meeting, instagram, messenger, telegram, other) | [optional][default to Other]
**direction** | Option<**Direction**> |  (enum: inbound, outbound) | [optional]
**occurred_at** | Option<**String**> | When it happened. Defaults to now. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


