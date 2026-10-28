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
**MaxPostAgeMinutes** | **int** | A post older than this when submitted is refused. | 
**Settlement** | **string** | none: settle records a payout made elsewhere. external: you pay from your own rails on campaign_payout.payable and settle with your reference. treasury: settle moves the money from your Zernio balance to the creator&#39;s Stripe account, and the creator sets up payouts from their campaign page. | 
**Economics** | [**CreatorCampaignEconomics**](CreatorCampaignEconomics.md) |  | 
**Caps** | [**CreatorCampaignCaps**](CreatorCampaignCaps.md) |  | 
**Branding** | [**CreatorCampaignBranding**](CreatorCampaignBranding.md) |  | 
**BudgetExhaustedAt** | **DateTime?** |  | 
**ClosedAt** | **DateTime?** |  | 
**PayableScannedAt** | **DateTime?** | Internal watermark of the payable scan. | 
**CreatedAt** | **DateTime** |  | 
**UpdatedAt** | **DateTime** |  | 
**HasOpenInvite** | **bool** | True once an open invite link was created. The link itself is returned only when it is created. | 
**ConsumedCents** | **int** | Budget used so far: earnings accrued, approved or adjusted against the campaign. | 
**ParticipantCount** | **int** |  | 
**SubmissionCounts** | [**CampaignSubmissionCounts**](CampaignSubmissionCounts.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

