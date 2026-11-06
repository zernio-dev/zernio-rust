# GetAutomationCatalog200ResponseTriggersInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**kind** | **Kind** |  (enum: ad_rule, event, scheduled) | 
**r#type** | **String** | `schedule`, or the Zernio event name. | 
**label** | Option<**String**> | Event triggers only. | [optional]
**subject** | Option<**String**> | What an event is about, such as `post` or `account`. | [optional]
**scope** | Option<**serde_json::Value**> | Which of `profileId` and `accountIds` an event trigger needs. | [optional]
**facts** | Option<[**Vec<models::GetAutomationCatalog200ResponseTriggersInnerFactsInner>**](GetAutomationCatalog200ResponseTriggersInnerFactsInner.md)> | The facts a `filter` can compare, for an event trigger. | [optional]
**subjects** | Option<**Vec<serde_json::Value>**> | Scheduled trigger only: what it can check (`post`), with the facts of each. | [optional]
**every** | Option<**Vec<String>**> |  | [optional]
**times** | Option<**serde_json::Value**> | Ad rule trigger only: the weekly set times it takes. | [optional]
**filter_operators** | Option<**Vec<String>**> |  | [optional]
**steps** | Option<**Vec<String>**> |  | [optional]
**boost** | Option<**serde_json::Value**> | Scheduled trigger only: the platforms, goals, most days and most boosts a day of `ads.boost_post`. | [optional]
**limits** | Option<**Vec<String>**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


