# Zernio.Model.WhatsAppTemplateComponent

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** |  | 
**Format** | **string** |  | 
**Text** | **string** | Static footer text | 
**Example** | [**WhatsAppBodyComponentExample**](WhatsAppBodyComponentExample.md) |  | [optional] 
**AddSecurityRecommendation** | **bool** | Add security recommendation text (authentication templates only) | [optional] 
**CodeExpirationMinutes** | **int** | OTP code expiry in minutes (authentication templates only) | [optional] 
**Buttons** | [**List&lt;WhatsAppTemplateButton&gt;**](WhatsAppTemplateButton.md) |  | 
**Cards** | [**List&lt;WhatsAppCarouselComponentCardsInner&gt;**](WhatsAppCarouselComponentCardsInner.md) | 2-10 cards. Meta requires all cards to share the same component structure; a mismatch surfaces as a rejected_reason. MARKETING category only. | 
**LimitedTimeOffer** | [**WhatsAppLimitedTimeOfferComponentLimitedTimeOffer**](WhatsAppLimitedTimeOfferComponentLimitedTimeOffer.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

