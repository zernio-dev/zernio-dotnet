# Zernio.Model.HubSpotSettings

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Zernio account ID of the HubSpot connection. | 
**Platform** | **string** |  | 
**HubId** | **string** | HubSpot portal (hub) ID. | 
**HubDomain** | **string** | HubSpot portal domain, when HubSpot reports one. | 
**Scopes** | **List&lt;string&gt;** | OAuth scopes the portal granted. | 
**SyncContacts** | **bool** | Whether Zernio creates HubSpot contacts for inbox contacts that match none. | 
**LogMessages** | **bool** | Whether Zernio logs inbox messages on HubSpot contact timelines. | 
**ReportDeals** | **bool** | Whether Zernio sends closed-won deals as Purchase events to the profile&#39;s event destinations. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

