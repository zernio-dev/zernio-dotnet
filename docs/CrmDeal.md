# Zernio.Model.CrmDeal
A HubSpot deal or a Salesforce Opportunity.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**ObjectType** | **string** |  | 
**Name** | **string** |  | 
**Stage** | **string** | HubSpot stage id (&#x60;closedwon&#x60;) or Salesforce &#x60;StageName&#x60; (&#x60;Closed Won&#x60;). | 
**Amount** | **decimal?** |  | 
**Currency** | **string** | ISO 4217. HubSpot sets it on multi-currency portals only. Salesforce gives the Opportunity&#39;s currency on multi-currency orgs, else the org currency read from its Currency Locale. | 
**CloseDate** | **DateOnly?** |  | 
**OwnerId** | **string** |  | 
**ContactIds** | **List&lt;string&gt;** | Associated HubSpot contacts, or the Opportunity&#39;s contact roles (primary first). | 
**CreatedAt** | **DateTime?** |  | 
**UpdatedAt** | **DateTime?** |  | 
**Url** | **string** |  | 
**Properties** | **Dictionary&lt;string, Object&gt;** |  | 
**Raw** | **Dictionary&lt;string, Object&gt;** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

