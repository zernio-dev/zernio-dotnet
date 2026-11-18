# Zernio.Model.CrmContact
A person in the connected CRM, in the same shape for HubSpot and Salesforce.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | The CRM&#39;s own id. | 
**ObjectType** | **string** | &#x60;lead&#x60; only on Salesforce. | 
**FirstName** | **string** |  | 
**LastName** | **string** |  | 
**Email** | **string** |  | 
**Phone** | **string** | The phone, else the mobile phone, as stored in the CRM. | 
**Company** | **string** | HubSpot &#x60;company&#x60;; Salesforce Lead &#x60;Company&#x60; or Contact Account name. | 
**OwnerId** | **string** |  | 
**CreatedAt** | **DateTime?** |  | 
**UpdatedAt** | **DateTime?** |  | 
**Url** | **string** | Opens the record in the CRM. | 
**Properties** | **Dictionary&lt;string, Object&gt;** | The native fields asked for with &#x60;properties&#x60;, by name. | 
**Raw** | **Dictionary&lt;string, Object&gt;** | The CRM&#39;s own record, only with &#x60;includeRaw&#x3D;true&#x60;. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

