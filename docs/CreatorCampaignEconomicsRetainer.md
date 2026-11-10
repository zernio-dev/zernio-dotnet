# Zernio.Model.CreatorCampaignEconomicsRetainer

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** |  | 
**Mode** | **string** | &#x60;standard&#x60; pays &#x60;amountCents&#x60; per period. &#x60;smart&#x60; guarantees it: the commission the creator earned in the period is topped up to &#x60;amountCents&#x60;. Smart needs &#x60;commission&#x60; and a linked store. | [optional] [default to ModeEnum.Standard]
**AmountCents** | **int** |  | 
**Period** | **string** | Weeks start Monday 00:00 UTC, months on the 1st. A period is paid within a day after it ends. A standard &#x60;once&#x60; retainer pays as soon as the posts are approved; a smart one when the campaign ends. | 
**RequiredApprovedPosts** | **int** | Posts approved within the period that it needs. 0 pays without posts. | 
**Commission** | [**CreatorCampaignCommissionTerms**](CreatorCampaignCommissionTerms.md) |  | [optional] 
**BudgetCents** | **int** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

