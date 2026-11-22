# Zernio.Model.UpdateCrmDealRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | [optional] 
**Stage** | **string** | HubSpot stage id, Salesforce &#x60;StageName&#x60; or HighLevel pipeline stage id. | [optional] 
**Amount** | **decimal?** |  | [optional] 
**Currency** | **string** | ISO 4217 code. Multi-currency HubSpot portals and Salesforce orgs only. | [optional] 
**CloseDate** | **DateOnly?** |  | [optional] 
**OwnerId** | **string** | An id from &#x60;GET /v1/crm/{accountId}/owners&#x60;. | [optional] 
**Properties** | [**Dictionary&lt;string, CrmNativePropertiesValue&gt;**](CrmNativePropertiesValue.md) | Native fields by internal name (HubSpot &#x60;lifecyclestage&#x60;, Salesforce &#x60;LeadSource&#x60; or &#x60;Industry__c&#x60;). On HighLevel, a record field (&#x60;source&#x60;, an opportunity &#x60;status&#x60;) or else a custom field id or key. A unified field of the same request wins over its native twin. &#x60;null&#x60; clears a field. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

