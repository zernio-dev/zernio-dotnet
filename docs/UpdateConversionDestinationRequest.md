# Zernio.Model.UpdateConversionDestinationRequest
At least one mutable field beyond `adAccountId` is required; the route returns 400 if no patch fields are provided. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AdAccountId** | **string** |  | 
**Name** | **string** |  | [optional] 
**Enabled** | **bool** | Setting &#x60;false&#x60; is equivalent to calling DELETE — the rule will appear as &#x60;inactive&#x60; afterwards.  | [optional] 
**AttributionType** | **string** |  | [optional] 
**PostClickAttributionWindowSize** | **int** | 365 only allowed for LEAD, PURCHASE, ADD_TO_CART, QUALIFIED_LEAD, SUBMIT_APPLICATION rule types.  | [optional] 
**ViewThroughAttributionWindowSize** | **int** | 365 only allowed for LEAD, PURCHASE, ADD_TO_CART, QUALIFIED_LEAD, SUBMIT_APPLICATION rule types.  | [optional] 
**ValueType** | **string** |  | [optional] 
**Value** | [**UpdateConversionDestinationRequestValue**](UpdateConversionDestinationRequestValue.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

