# StartSmsRegistrationRequestTollFree

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**business_name** | **String** |  | 
**corporate_website** | **String** |  | 
**phone_numbers** | **Vec<String>** |  | 
**use_case** | **String** |  | 
**use_case_summary** | **String** |  | 
**production_message_content** | **String** |  | 
**opt_in_workflow** | **String** | How recipients opt in to your messages. | 
**opt_in_workflow_image_urls** | **Vec<String>** | Screenshot URL(s) showing the opt-in flow (at least one). | 
**message_volume** | **MessageVolume** | Expected monthly message volume tier. (enum: 10, 100, 1,000, 10,000, 100,000, 250,000, 500,000, 750,000, 1,000,000, 5,000,000, 10,000,000+) | 
**additional_information** | **String** |  | 
**business_addr1** | **String** |  | 
**business_addr2** | Option<**String**> |  | [optional]
**business_city** | **String** |  | 
**business_state** | **String** |  | 
**business_zip** | **String** |  | 
**business_contact_first_name** | **String** |  | 
**business_contact_last_name** | **String** |  | 
**business_contact_email** | **String** |  | 
**business_contact_phone** | **String** |  | 
**business_registration_number** | **String** |  | 
**business_registration_type** | **String** | e.g. EIN (US), Companies House (UK), ABN (AU). | 
**business_registration_country** | **String** | ISO 3166-1 alpha-2. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


