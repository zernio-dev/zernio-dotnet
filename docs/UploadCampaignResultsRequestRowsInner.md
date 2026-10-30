# Zernio.Model.UploadCampaignResultsRequestRowsInner
Exactly one of `campaignId`, `utmCampaign` or `campaignName`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Date** | **DateOnly** | The day, at most 400 days ago. | 
**CampaignId** | **string** | The platform campaign id. | [optional] 
**UtmCampaign** | **string** | The &#x60;utm_campaign&#x60; value on the campaign&#39;s ads. | [optional] 
**CampaignName** | **string** | The campaign&#39;s name, matched case-insensitively. | [optional] 
**AdAccountId** | **string** | Platform ad account id. Narrows matching to one ad account. | [optional] 
**Values** | **Dictionary&lt;string, decimal&gt;** | Metric key (snake_case, up to 40 characters) to a non-negative number. 1 to 20 per row. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

