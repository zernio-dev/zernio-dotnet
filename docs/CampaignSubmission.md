# Zernio.Model.CampaignSubmission

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**CampaignId** | **string** |  | 
**ParticipantId** | **string** |  | 
**CreatorId** | **string** |  | 
**AccountId** | **string** | The creator account the post was published from. | 
**Platform** | **string** |  | 
**PlatformPostId** | **string** |  | 
**PlatformPostUrl** | **string** |  | 
**ExternalPostId** | **string** | The tracked external post (see /v1/external-posts). | 
**TrackingWindowId** | **string** |  | 
**MediaHash** | **string** |  | 
**SubmittedAt** | **DateTime** |  | 
**PostPublishedAt** | **DateTime?** |  | 
**Status** | **string** |  | 
**RejectReason** | **string** |  | 
**ReviewRound** | **int** | How many times the post was reopened after a reject. 0 until the first reopen. | 
**ReviewedBy** | **string** | User id of the reviewer. | 
**ReviewedAt** | **DateTime?** |  | 
**ViewsAtSubmission** | **int?** | Views when the post was submitted. They count toward earnings like every later view. | 
**ViewsLatest** | **int?** | Latest view count read for the post, frozen at the tracking window end. | 
**ViewsEligible** | **int?** | Views that count toward earnings: every view the platform reports for the post, including those before submission, read at the tracking window end at the latest: once the window completes or is cancelled, the last read at or before its end is final and this value stops moving. | 
**EngagementsLatest** | **int?** | The campaign engagement types summed at the latest read (all four on a views campaign), frozen at the tracking window end like &#x60;viewsEligible&#x60;. An &#x60;engagements&#x60; campaign earns on this count. | 
**ViewsPaid** | **int?** | Views from ads the creator ran: YouTube views from the advertising traffic source, X impressions beyond the organic ones. Null on other platforms and before the first read. On an organic-only campaign &#x60;viewsEligible&#x60; is the latest views minus these. | 
**PaidViewsReadAt** | **DateTime?** | When &#x60;viewsPaid&#x60; was last read. YouTube refreshes every 6 hours and reports ad views up to 2 days late; X about once a day while the post is under 30 days old. | 
**LastAccruedViews** | **int** |  | 
**AccruedCents** | **int** |  | 
**ApprovedCents** | **int** |  | 
**AuthenticityScore** | **int?** |  | 
**AuthenticityConfidence** | **decimal?** |  | 
**Flags** | [**List&lt;CampaignSubmissionFlag&gt;**](CampaignSubmissionFlag.md) |  | 
**CreatedAt** | **DateTime** |  | 
**UpdatedAt** | **DateTime** |  | 
**Creator** | [**WebhookPayloadCampaignSubmissionCreator**](WebhookPayloadCampaignSubmissionCreator.md) |  | 
**Authenticity** | [**CampaignSubmissionAuthenticity**](CampaignSubmissionAuthenticity.md) |  | 
**EarnedCents** | **int** | approvedCents once approved, otherwise accruedCents. | 
**ReleasedCents** | **int** | Approved cents whose hold is over, so payable or already paid out. 0 unless approved. | 
**PaidOutCents** | **int** | What rejecting this post could not take back now: releasedCents beyond the creator&#39;s payable balance. It stays paid; the dashboard warns before such a reject. | 
**Window** | [**CampaignSubmissionWindow**](CampaignSubmissionWindow.md) |  | 
**Post** | [**CampaignSubmissionPost**](CampaignSubmissionPost.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

