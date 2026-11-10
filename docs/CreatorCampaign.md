# Zernio.Model.CreatorCampaign

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**UserId** | **string** | The workspace billing owner the campaign belongs to. | 
**ProfileId** | **string** | The profile that scopes the campaign: API keys, teammates and webhooks scoped to it reach the campaign. | 
**Kind** | **string** |  | 
**Name** | **string** |  | 
**BrandName** | **string** |  | 
**Status** | **string** | draft until activated; active accepts submissions and accrues; paused stops new submissions; closed is final. | 
**Type** | **string** | Same as economics.type. | 
**Currency** | **string** |  | 
**Platforms** | **List&lt;CreatorCampaign.PlatformsEnum&gt;** |  | 
**ContentRules** | **string** | Free-text rules shown to creators on the join page. | 
**StartsAt** | **DateTime?** |  | 
**EndsAt** | **DateTime?** | No new submissions after this time; the campaign closes once every tracking window had its final read. | 
**TrackingDays** | **int** | How long each submitted post is tracked. | 
**HoldDays** | **int** | Days approved earnings are held before they become payable. | 
**MaxPostAgeMinutes** | **int?** | A post older than this many minutes when submitted is refused. Null (the default) accepts any age. Either way, a post published before the campaign started (&#x60;startsAt&#x60;, or &#x60;activatedAt&#x60; without one) is refused. | 
**ActivatedAt** | **DateTime?** | When the campaign was first activated. Without &#x60;startsAt&#x60;, posts must be published after this moment. | 
**Settlement** | **string** | none: settle records a payout made elsewhere. external: you pay from your own rails on campaign_payout.payable and settle with your reference. treasury: you pay by card with a payout batch and Zernio pays each creator in your name 7 days after the charge. | 
**Economics** | [**CreatorCampaignEconomics**](CreatorCampaignEconomics.md) |  | 
**Caps** | [**CreatorCampaignCaps**](CreatorCampaignCaps.md) |  | 
**Branding** | [**CreatorCampaignBranding**](CreatorCampaignBranding.md) |  | 
**BudgetExhaustedAt** | **DateTime?** |  | 
**ClosedAt** | **DateTime?** |  | 
**PayableScannedAt** | **DateTime?** | Internal watermark of the payable scan. | 
**JoinApproval** | **string** | auto: creators who join through the open link are active at once. manual: they land &#x60;pending&#x60; until you approve or deny them. Personal invites are never held. | 
**RequireDraftApproval** | **bool** | Creators upload a draft for review first, and submit the live post for an approved draft (&#x60;draftId&#x60;). | 
**StoreAccountId** | **string** | The connected store (Shopify or WooCommerce) whose orders pay commission and whose products creators can ask as samples. Null when the campaign has neither. | 
**SampleProducts** | [**List&lt;CreatorCampaignSampleProduct&gt;**](CreatorCampaignSampleProduct.md) | Products creators can ask a free sample of. | 
**SampleContentDueDays** | **int** | Days after a sample is approved before a creator with no post since shows as owing content (&#x60;contentOwed&#x60;). | 
**CreatedAt** | **DateTime** |  | 
**UpdatedAt** | **DateTime** |  | 
**HasOpenInvite** | **bool** | True once an open invite link was created. The link itself is returned only when it is created. | 
**ConsumedCents** | **int** | Budget used so far: earnings accrued, approved or adjusted against the campaign. | 
**ParticipantCount** | **int** |  | 
**SubmissionCounts** | [**CampaignSubmissionCounts**](CampaignSubmissionCounts.md) |  | 
**PayableCents** | **int** | What the campaign&#39;s creators can be paid now, summed over every participant&#39;s payable balance. | 
**LandingUrl** | **string** | The page creator tracking links open. | [optional] 
**CodeDiscountPercent** | **int?** | What each creator discount code takes off. | [optional] 
**AutoPayout** | [**CreatorCampaignAutoPayout**](CreatorCampaignAutoPayout.md) |  | [optional] 
**PendingParticipantCount** | **int** | Creators who asked to join through the open link and wait for a decision. Not counted in &#x60;participantCount&#x60;. | 
**DraftCounts** | [**CampaignDraftCounts**](CampaignDraftCounts.md) |  | 
**SampleCounts** | [**CampaignSampleCounts**](CampaignSampleCounts.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

