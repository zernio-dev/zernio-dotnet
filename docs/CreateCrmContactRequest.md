# Zernio.Model.CreateCrmContactRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**FirstName** | **string** |  | [optional] 
**LastName** | **string** |  | [optional] 
**Email** | **string** |  | [optional] 
**Phone** | **string** |  | [optional] 
**Company** | **string** |  | [optional] 
**OwnerId** | **string** | An id from &#x60;GET /v1/crm/{accountId}/owners&#x60;. | [optional] 
**Properties** | [**Dictionary&lt;string, CrmNativePropertiesValue&gt;**](CrmNativePropertiesValue.md) | Native fields by internal name (HubSpot &#x60;lifecyclestage&#x60;, Salesforce &#x60;LeadSource&#x60; or &#x60;Industry__c&#x60;). On HighLevel, a record field (&#x60;source&#x60;, an opportunity &#x60;status&#x60;) or else a custom field id or key. A unified field of the same request wins over its native twin. &#x60;null&#x60; clears a field. | [optional] 
**CreateAs** | **string** | Salesforce only. Defaults to the connection&#39;s &#x60;createAs&#x60; setting. Ignored on HubSpot and HighLevel. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

