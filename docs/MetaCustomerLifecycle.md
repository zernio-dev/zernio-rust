# MetaCustomerLifecycle

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**strategy** | **Strategy** | `all_customers` is \"Maximize conversions from all customers\". `new_customers` is \"Acquire new customers\" (excludes existing customers). `new_customers_excluding_engaged` also excludes people who engaged with you but have not bought yet.  (enum: all_customers, new_customers, new_customers_excluding_engaged) | 
**existing_customer_audience_ids** | Option<**Vec<String>**> | Custom audience ids that define your existing customers. Required with both new_customers strategies (Meta answers 400 subcode 1870251 without them); not allowed with all_customers. | [optional]
**engaged_audience_ids** | Option<**Vec<String>**> | Custom audience ids of people who engaged but have not bought. Required with new_customers_excluding_engaged, not allowed with the other strategies. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


