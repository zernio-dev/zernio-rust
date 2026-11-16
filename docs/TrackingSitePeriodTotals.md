# TrackingSitePeriodTotals

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**visits** | Option<**i32**> | Page views without bots. | [optional]
**bots** | Option<**i32**> | Page views from bots. | [optional]
**consented** | Option<**i32**> | Page views with ad storage consent, at most `visits`. | [optional]
**purchases** | Option<**i32**> | Purchases recorded on the site. | [optional]
**recovered** | Option<**i32**> | Purchases with ad consent for which no browser pixel fired, so only the server reported them. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


