# Zernio.Model.CrmDeal
A HubSpot deal, a Salesforce Opportunity or a HighLevel opportunity.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**ObjectType** | **string** |  | 
**Name** | **string** |  | 
**Stage** | **string** | HubSpot stage id (&#x60;closedwon&#x60;), Salesforce &#x60;StageName&#x60; (&#x60;Closed Won&#x60;) or HighLevel pipeline stage id. A HighLevel opportunity&#39;s won or lost &#x60;status&#x60; is a native field (&#x60;properties&#x3D;status&#x60;). | 
**Amount** | **decimal?** |  | 
**Currency** | **string** | ISO 4217. HubSpot sets it on multi-currency portals only. Salesforce gives the Opportunity&#39;s currency on multi-currency orgs, else the org currency read from its Currency Locale. Null on HighLevel. | 
**CloseDate** | **DateOnly?** | Null on HighLevel, whose opportunities have no close date. | 
**OwnerId** | **string** |  | 
**ContactIds** | **List&lt;string&gt;** | Associated HubSpot contacts, the Opportunity&#39;s contact roles (primary first), or the HighLevel opportunity&#39;s contact. | 
**CreatedAt** | **DateTime?** |  | 
**UpdatedAt** | **DateTime?** |  | 
**Url** | **string** |  | 
**Properties** | **Dictionary&lt;string, Object&gt;** |  | 
**Raw** | **Dictionary&lt;string, Object&gt;** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

