# Zernio.Model.CreatorPortalDraft
One version of a draft the creator uploaded for review.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Pass as &#x60;draftId&#x60; when submitting the live post of an approved draft, or as &#x60;revisionOf&#x60; to answer a revision request. | 
**ChainId** | **string** |  | 
**VarVersion** | **int** |  | 
**RevisionOf** | **string** |  | 
**Status** | **string** |  | 
**MediaUrl** | **string** |  | 
**MediaType** | **string** |  | 
**Caption** | **string** |  | 
**ReviewNote** | **string** |  | 
**Comments** | [**List&lt;CreatorPortalDraftCommentsInner&gt;**](CreatorPortalDraftCommentsInner.md) |  | 
**SubmittedAt** | **DateTime** |  | 
**ReviewedAt** | **DateTime?** |  | 
**SubmissionId** | **string** | The live post submitted for this draft. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

