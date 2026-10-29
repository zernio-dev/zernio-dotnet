# Zernio.Model.BrandedCallingIdentity

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**EnterpriseId** | **string** |  | [optional] 
**DisplayName** | **string** |  | [optional] 
**CallReasons** | **List&lt;string&gt;** |  | [optional] 
**CallReasonsPreApproved** | **bool** | Every call reason matches the carrier catalogue (GET /v1/branded-calling/call-reasons); anything else is vetted by hand and takes longer. | [optional] 
**LogoUrl** | **string** | The image you sent. Zernio hosts the 256x256 BMP the carriers require. | [optional] 
**Authorizer** | [**BrandedCallingIdentityAuthorizer**](BrandedCallingIdentityAuthorizer.md) |  | [optional] 
**References** | [**BrandedCallingReferences**](BrandedCallingReferences.md) |  | [optional] 
**Status** | **string** | Verification status:  - requested: in Zernio review - changes_requested: answer the review (PATCH) - pending_email_verification: confirm the code emailed to the authorizer - in_review: with the carrier vetting team - verified: attach numbers - rejected: fix and PATCH to resubmit - suspended: an infringement claim is open - expired: the yearly verification lapsed - permanently_rejected: terminal  | [optional] 
**RejectionReasons** | [**List&lt;BrandedCallingIdentityRejectionReasonsInner&gt;**](BrandedCallingIdentityRejectionReasonsInner.md) |  | [optional] 
**ReviewNote** | **string** | The open change request, as text. | [optional] 
**ReviewRequest** | [**BrandedCallingIdentityReviewRequest**](BrandedCallingIdentityReviewRequest.md) |  | [optional] 
**EmailVerifiedAt** | **DateTime?** |  | [optional] 
**SubmittedAt** | **DateTime?** |  | [optional] 
**VerifiedAt** | **DateTime?** |  | [optional] 
**ExpiringAt** | **DateTime?** | Verification lasts one year; Zernio resubmits 30 days before this date. | [optional] 
**Numbers** | [**List&lt;BrandedCallingIdentityNumber&gt;**](BrandedCallingIdentityNumber.md) |  | [optional] 
**CreatedAt** | **DateTime?** |  | [optional] 
**UpdatedAt** | **DateTime?** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

