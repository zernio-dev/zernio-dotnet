# Zernio.Model.CreateHighDemandPeriodRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Zernio SocialAccount id used to resolve the Meta token. | 
**CampaignId** | **string** | Platform campaign id. Exactly one of campaignId / adSetId. | [optional] 
**AdSetId** | **string** | Platform ad set id. Exactly one of campaignId / adSetId. | [optional] 
**BudgetValue** | **decimal** | With ABSOLUTE, a budget in the ad account&#39;s currency in WHOLE units (50 &#x3D; $50.00). With MULTIPLIER, a factor of the existing budget (2 &#x3D; double it) and NOT a currency amount. | 
**BudgetValueType** | **string** |  | 
**TimeStart** | **int** | Unix seconds, on a 15-minute boundary (:00, :15, :30, :45). | 
**TimeEnd** | **int** | Unix seconds, on a 15-minute boundary and after timeStart. | 
**RecurrenceType** | **string** |  | [optional] 
**Currency** | **string** | Ad account currency, for the ABSOLUTE minor-unit conversion. Ignored for MULTIPLIER. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

