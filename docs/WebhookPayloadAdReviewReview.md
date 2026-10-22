# Zernio.Model.WebhookPayloadAdReviewReview

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Status** | **string** |  | 
**Raw** | **string** | Platform-native status string, forwarded verbatim (Meta &#x60;ACTIVE&#x60; / &#x60;DISAPPROVED&#x60;, TikTok &#x60;DISABLE&#x60;, ...). | 
**Reasons** | [**List&lt;WebhookPayloadAdReviewReviewReasonsInner&gt;**](WebhookPayloadAdReviewReviewReasonsInner.md) | Why the platform rejected the ad, when it says. Always empty on &#x60;approved&#x60;. Most networks only return a generic message today. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

