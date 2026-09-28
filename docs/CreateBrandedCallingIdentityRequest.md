# Zernio.Model.CreateBrandedCallingIdentityRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EnterpriseId** | **string** | A business from POST /v1/branded-calling/enterprises. | 
**DisplayName** | **string** | Shown on the callee&#39;s screen. No emoji. | 
**CallReasons** | **List&lt;string&gt;** | 1 to 10 reasons you call, each up to 64 characters. Pick from GET /v1/branded-calling/call-reasons to skip manual vetting. | 
**LogoUrl** | **string** | HTTPS URL of a PNG, JPEG, WebP or SVG logo. Zernio converts it to the 256x256 BMP the carriers require and hosts it. | [optional] 
**Authorizer** | [**CreateBrandedCallingIdentityRequestAuthorizer**](CreateBrandedCallingIdentityRequestAuthorizer.md) |  | 
**References** | [**BrandedCallingReferences**](BrandedCallingReferences.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

