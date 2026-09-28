# Zernio.Model.UpdateBrandedCallingIdentityRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DisplayName** | **string** | Shown on the callee&#39;s screen. No emoji. | [optional] 
**CallReasons** | **List&lt;string&gt;** | 1 to 10 reasons you call, each up to 64 characters. Pick from GET /v1/branded-calling/call-reasons to skip manual vetting. | [optional] 
**LogoUrl** | **string** | HTTPS URL of a PNG, JPEG, WebP or SVG logo. Zernio converts it to the 256x256 BMP the carriers require and hosts it. | [optional] 
**Authorizer** | [**CreateBrandedCallingIdentityRequestAuthorizer**](CreateBrandedCallingIdentityRequestAuthorizer.md) |  | [optional] 
**References** | [**BrandedCallingReferences**](BrandedCallingReferences.md) |  | [optional] 
**ReviewAnswers** | [**Dictionary&lt;string, UpdateBrandedCallingIdentityRequestReviewAnswersValue&gt;**](UpdateBrandedCallingIdentityRequestReviewAnswersValue.md) | One entry per point id of the open reviewRequest. | [optional] 
**ReviewNote** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

