# AdAppliedDefaults

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | Option<**String**> | Sent when `name` was omitted: `Ad <YYYY-MM-DD HH:MM:SS>` in UTC. | [optional]
**goal** | Option<**String**> | Sent when `goal` was omitted: the goal Zernio inferred.  - `lead_generation`: with a `leadGenFormId`. - `app_promotion`: when `promotedObject` names an app. - `conversions`: with `promotedObject.pixelId` and `customEventType`. - `traffic`: when the ad has a link (`linkUrl`, a carousel card, `creatives[].linkUrl`, `dynamicCreative.linkUrls` or a LinkedIn carousel card). - `engagement`: otherwise.  Each applies only when the platform offers it, falling back to `engagement`, then `awareness`, then the platform's first goal. Never inferred with `existingCampaignId`, `smartPlus` or the LinkedIn spotlight, follower and jobs formats: those still return 400 without `goal`. | [optional]
**budget_type** | Option<**BudgetType**> | Sent when `budgetAmount` came without `budgetType`. (enum: daily) | [optional]
**end_date** | Option<**String**> | Sent when a lifetime budget had no `endDate`: 7 days after the start. A daily budget never gets one and runs until paused.  - A start with an offset (or no start) gets a UTC instant. - An offset-less start gets an offset-less end, read in the ad account timezone like the start. - A date-only start gets the date 6 days later, which runs to 23:59:59. | [optional]
**countries** | Option<**Vec<String>**> | Sent when the request sent no countries and the ad gets the long-standing United States default. Not sent on attach, Google Performance Max or Demand Gen, or a Google ad group joining `existingCampaignId`, which keep their own geo. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


