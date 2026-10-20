# Zernio.Model.GoogleAdsUserAccessInvitationResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **string** |  | [optional] 
**EmailAddress** | **string** |  | [optional] 
**AccessRole** | **GoogleAdsAccessRole** |  | [optional] 
**Status** | **string** | PENDING once the email is sent; PENDING_APPROVAL while Google waits for a second admin&#39;s multi-party approval. | [optional] 
**InvitationId** | **string** | Null on validateOnly and while the invitation awaits multi-party approval. | [optional] 
**MultiPartyAuthReviewId** | **string** | Google&#39;s multi-party approval review id when status is PENDING_APPROVAL. | [optional] 
**ValidateOnly** | **bool** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

