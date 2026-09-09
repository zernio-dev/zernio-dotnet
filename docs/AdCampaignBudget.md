# Zernio.Model.AdCampaignBudget

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Amount** | **decimal** |  | 
**Type** | **string** |  | 
**AmountMicros** | **string** | Google only. Exact decimal micros; DAILY uses amount_micros and CUSTOM_PERIOD uses total_amount_micros. | [optional] 
**ExplicitlyShared** | **bool?** | Google only. True for a shared budget; null when unavailable. Shared writes require allowSharedBudgetUpdate&#x3D;true; unknown sharing status cannot be overridden. | [optional] 
**ResourceName** | **string** | Google only. campaign_budget.resource_name, or null when unavailable. | [optional] 
**DeliveryMethod** | **string** | Google only. campaign_budget.delivery_method, typically STANDARD, or null when unavailable. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

