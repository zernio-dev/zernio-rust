# GetEventsAccuracy200ResponseDestinationsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**rule_id** | Option<**String**> | The forwarding rule. | [optional]
**profile_id** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**platform** | Option<**String**> | Ad platform, such as `metaads` or `googleads`. | [optional]
**account_name** | Option<**String**> |  | [optional]
**destination_id** | Option<**String**> |  | [optional]
**sales** | Option<**i32**> | Real sales in the period from the sources the rule takes. | [optional]
**sent** | Option<**i32**> | Sales a send was tried for. | [optional]
**accepted** | Option<**i32**> | Sales the platform accepted, by the latest attempt. | [optional]
**failed** | Option<**i32**> |  | [optional]
**retrying** | Option<**i32**> |  | [optional]
**not_sent** | Option<**i32**> | Sales never sent: no ad consent, no identifier the platform matches on, or left out by the rule's event names. | [optional]
**accuracy** | Option<**f64**> | `accepted / sent`, from 0 to 1. `null` with no sale sent. | [optional]
**deliveries** | Option<[**models::GetEventsAccuracy200ResponseDestinationsInnerDeliveries**](GetEventsAccuracy200ResponseDestinationsInnerDeliveries.md)> |  | [optional]
**r#match** | Option<[**models::GetEventsAccuracy200ResponseDestinationsInnerMatch**](GetEventsAccuracy200ResponseDestinationsInnerMatch.md)> |  | [optional]
**match_rate** | Option<**f64**> | `match.identified / match.events`. `null` with nothing sent. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


