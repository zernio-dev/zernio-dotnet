# Zernio.Model.CampaignDraft
One version of a creator's content, uploaded for review before it is published. A revision is a new version in the same `chainId` with `version` + 1 and `revisionOf` set to the version it answers.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**CampaignId** | **string** |  | 
**ParticipantId** | **string** |  | 
**Creator** | [**CreatorCampaignAdResultsSubmissionsInnerCreator**](CreatorCampaignAdResultsSubmissionsInnerCreator.md) |  | 
**ChainId** | **string** | The id of the first version of the chain. | 
**VarVersion** | **int** |  | 
**RevisionOf** | **string** | The version this one answers; null on version 1. | 
**MediaUrl** | **string** |  | 
**MediaType** | **string** |  | 
**Caption** | **string** |  | 
**Status** | **string** | submitted: waits for review. approved: the creator may publish it. revision_requested: the creator should upload a new version. rejected: final. | 
**ReviewNote** | **string** | The note sent with a revision request, or the rejection reason. | 
**ReviewedAt** | **DateTime?** |  | 
**SubmittedAt** | **DateTime** |  | 
**Comments** | [**List&lt;CampaignDraftCommentsInner&gt;**](CampaignDraftCommentsInner.md) | Review comments on this version, in video order. | 
**SubmissionId** | **string** | The live post submitted for this draft, once the creator published it. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

