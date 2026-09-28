# Zernio.Model.RcsAgentProfile
The agent's public profile. At least one of phone, website or email is required.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Description** | **string** |  | 
**LogoUrl** | **string** | 224x224, max 50 KB. Upload any image through POST /v1/rcs/assets to get a compliant URL. | 
**HeroUrl** | **string** | Banner, 1440x448, max 200 KB. Upload through POST /v1/rcs/assets. | 
**BrandColor** | **string** | Hex colour, e.g. #1A73E8. Needs 4.5:1 contrast against white. | 
**PrivacyPolicyUrl** | **string** |  | 
**TermsUrl** | **string** |  | 
**Phone** | [**RcsAgentProfilePhone**](RcsAgentProfilePhone.md) |  | [optional] 
**Website** | [**RcsAgentProfileWebsite**](RcsAgentProfileWebsite.md) |  | [optional] 
**Email** | [**RcsAgentProfileEmail**](RcsAgentProfileEmail.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

