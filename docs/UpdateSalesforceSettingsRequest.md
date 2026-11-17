# Zernio.Model.UpdateSalesforceSettingsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**SyncContacts** | **bool** | Create a Lead or Contact for an inbox contact that matches nobody by phone (any phone field) or email. A match is linked as it is and never updated. | [optional] 
**LogMessages** | **bool** | Log inbound and outbound inbox messages as one conversation Task per person, channel and day. | [optional] 
**CreateAs** | **string** | What a person new to Salesforce is created as. Leads get Company &#x60;[not provided]&#x60;. | [optional] 
**LogDeliveryStatus** | **bool** | Mark sent messages in the transcript as delivered, read or failed. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

