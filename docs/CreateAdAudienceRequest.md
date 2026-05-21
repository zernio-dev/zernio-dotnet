# Zernio.Model.CreateAdAudienceRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** |  | 
**AdAccountId** | **string** | Platform ad account ID. Must start with act_ for Meta; bare platform id for others (Google customer id, X/TikTok/LinkedIn/Pinterest account id). | 
**Name** | **string** |  | 
**Description** | **string** |  | [optional] 
**Type** | **string** |  | 
**PixelId** | **string** | Required for website audiences | [optional] 
**RetentionDays** | **int** | Required for website audiences | [optional] 
**SourceAudienceId** | **string** | Required for lookalike audiences | [optional] 
**Country** | **string** | 2-letter code, required for lookalike audiences | [optional] 
**Ratio** | **decimal** | Required for lookalike audiences | [optional] 
**Rule** | **Object** | Pixel event rule for website audiences (optional) | [optional] 
**CustomerFileSource** | **string** | Data source declaration for GDPR compliance (customer_list only) | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

