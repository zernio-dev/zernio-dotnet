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
**LogDeliveryStatus** | **bool** | Whether Zernio keeps the delivery status (sent, delivered, read, played, failed) of logged outgoing messages up to date on their HubSpot timeline entries. Only applies while &#x60;logMessages&#x60; is on. Defaults to &#x60;true&#x60;. | 
**ContactDefaults** | **Dictionary&lt;string, string&gt;** | Values Zernio sets on contacts it creates, keyed by HubSpot internal property name, for properties the portal requires on create (for example &#x60;lifecyclestage: lead&#x60;). The contact&#39;s own name, email and phone win. Empty object when none. | 
**SyncIssue** | [**HubSpotSettingsSyncIssue**](HubSpotSettingsSyncIssue.md) |  | 
**ReportDeals** | **bool** | Whether Zernio sends closed-won deals as Purchase events to the profile&#39;s event destinations. | 
**UseDealsAsResults** | **bool** | Whether closed-won deals count as sales on the ad campaign that brought their contact, in campaign results and ad rules. | 
**QualifiedLeads** | [**HubSpotQualifiedLeads**](HubSpotQualifiedLeads.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

