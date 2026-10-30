# Zernio.Model.WebhookPayloadCampaignSubmissionSubmission

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**Platform** | **string** |  | 
**PlatformPostId** | **string** |  | 
**PlatformPostUrl** | **string** |  | 
**Status** | **string** |  | 
**ViewsAtSubmission** | **int?** |  | 
**ViewsEligible** | **int?** | Views that count toward earnings at the latest read. | 
**EngagementsLatest** | **int?** | The campaign engagement types summed at the latest read. An engagements campaign earns on this count. | 
**ViewsPaid** | **int?** | Views from ads, on YouTube and X. Null elsewhere or before the first read. | 
**Flags** | [**List&lt;WebhookPayloadCampaignSubmissionSubmissionFlagsInner&gt;**](WebhookPayloadCampaignSubmissionSubmissionFlagsInner.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

