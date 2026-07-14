# Zernio.Model.LinkedInAdsPlatformDataJobs
POST /v1/ads/create only. Dynamic Jobs Ad promoting your open roles, personalized with the viewer's profile photo. Requires goal job_applicants and a Company Page with active job postings. headline and buttonLabel take exactly one of preApproved or custom. logoUrl and organizationName default to the Company Page's. Mutually exclusive with the other creative sources. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Headline** | [**LinkedInAdsPlatformDataJobsHeadline**](LinkedInAdsPlatformDataJobsHeadline.md) |  | 
**ButtonLabel** | [**LinkedInAdsPlatformDataJobsButtonLabel**](LinkedInAdsPlatformDataJobsButtonLabel.md) |  | 
**LogoUrl** | **string** |  | [optional] 
**OrganizationName** | **string** |  | [optional] 
**ShowMemberProfilePhoto** | **bool** | Defaults to true. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

