# Zernio.Model.CreateCommerceOrderEditRequest
Pass at least one of add or quantities.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Connected store SocialAccount id. | 
**Add** | [**List&lt;CreateCommerceOrderEditRequestAddInner&gt;**](CreateCommerceOrderEditRequestAddInner.md) |  | [optional] 
**Quantities** | [**List&lt;CreateCommerceOrderEditRequestQuantitiesInner&gt;**](CreateCommerceOrderEditRequestQuantitiesInner.md) |  | [optional] 
**NotifyCustomer** | **bool** |  | [optional] [default to false]
**StaffNote** | **string** |  | [optional] 
**ValidateOnly** | **bool** | Return the edited totals without changing the order. | [optional] [default to false]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

