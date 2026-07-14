# Zernio.Model.LinkedInAdsPlatformDataFollower
POST /v1/ads/create only. Dynamic Follower Ad promoting the Company Page. Supported goals: engagement, awareness. headline and description take exactly one of preApproved or custom. Mutually exclusive with the other creative sources. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Headline** | [**LinkedInAdsPlatformDataFollowerHeadline**](LinkedInAdsPlatformDataFollowerHeadline.md) |  | 
**Description** | [**LinkedInAdsPlatformDataFollowerDescription**](LinkedInAdsPlatformDataFollowerDescription.md) |  | 
**CallToAction** | **string** |  | 
**LogoUrl** | **string** |  | [optional] 
**OrganizationName** | **string** |  | [optional] 
**ShowMemberProfilePhoto** | **bool** | Defaults to true. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

