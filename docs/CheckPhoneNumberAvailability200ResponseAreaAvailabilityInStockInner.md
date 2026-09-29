# CheckPhoneNumberAvailability200ResponseAreaAvailabilityInStockInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ndc** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**count** | Option<**i32**> | Numbers we can sell there: the carrier count minus the numbers we hold back (WhatsApp refused them or another order holds them). | [optional]
**ndcs** | Option<**Vec<String>**> | Every area code of the city, deepest first (Madrid: 915, 911, 910, ...). `ndc` is the one an order is placed against. | [optional]
**aliases** | Option<**Vec<String>**> | Other names the area answers to, present only when it has some (Milano for Milan, Sevilla for Seville). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


