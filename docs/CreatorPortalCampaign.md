# Zernio.Model.CreatorPortalCampaign
The campaign as a creator sees it: terms, never the budget.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | The campaign id, as in a link-recovery URL. | 
**Name** | **string** |  | 
**BrandName** | **string** |  | 
**LogoUrl** | **string** |  | 
**Theme** | **Object** | Same keys as the &#x60;welcomeTheme&#x60; parameter of &#x60;GET /v1/connect/{platform}&#x60;. | 
**Status** | **string** |  | 
**Platforms** | **List&lt;string&gt;** |  | 
**ContentRules** | **string** |  | 
**StartsAt** | **DateTime?** |  | 
**EndsAt** | **DateTime?** |  | 
**StartedAt** | **DateTime** | Posts published before this moment do not count: &#x60;startsAt&#x60;, else when the campaign went live. | 
**Currency** | **string** |  | 
**Economics** | [**CreatorPortalEconomics**](CreatorPortalEconomics.md) |  | 
**MaxPostAgeMinutes** | **int?** | A post must be submitted within this many minutes of publishing. Null means any age. Either way, only posts published after the campaign started are accepted. | 
**HoldDays** | **int** | Days approved earnings stay owed before they become payable. | 
**TrackingDays** | **int** | Days each submitted post is tracked for views. | 
**MaxAccountsPerParticipant** | **int?** | How many connected accounts can submit posts. Null means no limit. | 
**JoinApproval** | **string** | manual: a creator who joins through the open link waits &#x60;pending&#x60; until the campaign team accepts them. | 
**RequireDraftApproval** | **bool** | The creator uploads a draft for review first, and submits the live post for an approved draft. | 
**SampleProducts** | [**List&lt;CreatorCampaignSampleProduct&gt;**](CreatorCampaignSampleProduct.md) | Products the creator can ask a free sample of; empty when the campaign offers none. | 
**SampleContentDueDays** | **int** | Days after a sample is approved by which a post is expected. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

