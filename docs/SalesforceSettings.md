# Zernio.Model.SalesforceSettings

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Zernio account ID of the Salesforce connection. | 
**Platform** | **string** |  | 
**OrgId** | **string** | 18-character Salesforce organization ID. | 
**OrgName** | **string** | The org&#39;s name, when the connected user can read it. | 
**VarEnvironment** | **string** | Whether the org was connected through login.salesforce.com or test.salesforce.com. | 
**InstanceUrl** | **string** | The org&#39;s API host, for example &#x60;https://acme.my.salesforce.com&#x60;. | 
**InstalledBy** | **string** | Email or username of the Salesforce user who connected the org. | 
**SyncContacts** | **bool** | Whether Zernio creates a Lead or Contact (per &#x60;createAs&#x60;) for an inbox contact that matches nobody by phone or email. | 
**LogMessages** | **bool** | Whether Zernio logs inbox messages. Each person, channel and UTC day gets one completed Task (subject &#x60;WhatsApp conversation · 2026-11-17&#x60;) whose Description holds the transcript; a day past 32,000 characters continues in a Task marked \&quot;(part 2)\&quot;. | 
**CreateAs** | **string** | What a person new to Salesforce is created as. | 
**LogDeliveryStatus** | **bool** | Whether sent messages in the transcript are marked delivered, read or failed. | 
**SyncIssue** | [**SalesforceSettingsSyncIssue**](SalesforceSettingsSyncIssue.md) |  | 
**UseOpportunitiesInResults** | **bool** | Whether closed-won Opportunities count as sales (Amount, in the Opportunity&#39;s or the org&#39;s currency) on the ad campaign named by their Primary Campaign Source, in campaign results and ad rules. Lost or reopened Opportunities stop counting. | 
**ReportOpportunitiesToAds** | **bool** | Whether Zernio sends newly closed-won Opportunities as Purchase events (source &#x60;salesforce&#x60;) to the profile&#39;s event destinations. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

