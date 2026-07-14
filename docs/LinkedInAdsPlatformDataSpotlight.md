# Zernio.Model.LinkedInAdsPlatformDataSpotlight
POST /v1/ads/create only. Dynamic Spotlight Ad personalized with the viewer's profile photo. Supported goals: traffic, awareness. logoUrl and organizationName default to the Company Page's; set them explicitly if LinkedIn rejects the create with a 404. Mutually exclusive with the other creative sources. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Headline** | **string** |  | 
**Description** | **string** | Mutually exclusive with backgroundImageUrl. | [optional] 
**CallToAction** | **string** | Button label text. | 
**LandingUrl** | **string** |  | 
**LogoUrl** | **string** |  | [optional] 
**OrganizationName** | **string** |  | [optional] 
**ShowMemberProfilePhoto** | **bool** | Defaults to true. | [optional] 
**BackgroundImageUrl** | **string** | Custom background. Replaces the description and the profile photo. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

