# Zernio.Model.UpdateHubSpotSettingsRequestQualifiedLeads
Count a contact as a `QualifiedLead` event once `property` holds one of `values`, checked every 15 minutes. It carries the contact's hashed email and phone and its ad campaign, and counts in campaign results and ad rules.  It goes to the forwarding rules that name `QualifiedLead`, and is retracted when the contact drops to another value. Contacts that qualified before the rule was turned on are not counted. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Enabled** | **bool** |  | 
**Property** | **string** | HubSpot internal name of the contact property, for example &#x60;lifecyclestage&#x60;. | 
**Values** | **List&lt;string&gt;** | The values that count as qualified. At least one while &#x60;enabled&#x60; is true. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

