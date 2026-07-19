# UpdateGoogleBusinessPlaceActionRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** | Resource name of the place action link (e.g. locations/123/placeActionLinks/456) | 
**uri** | Option<**String**> | New action URL. At least one of uri or placeActionType is required (enforced server-side; not modeled as anyOf because required-only anyOf branches break SDK generators). | [optional]
**place_action_type** | Option<**PlaceActionType**> | New action type (enum: APPOINTMENT, ONLINE_APPOINTMENT, DINING_RESERVATION, FOOD_ORDERING, FOOD_DELIVERY, FOOD_TAKEOUT, SHOP_ONLINE) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


