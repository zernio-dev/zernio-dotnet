# Zernio.Model.CampaignSample
A free product sample a creator asked for.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**CampaignId** | **string** |  | 
**ParticipantId** | **string** |  | 
**Creator** | [**CreatorCampaignAdResultsSubmissionsInnerCreator**](CreatorCampaignAdResultsSubmissionsInnerCreator.md) |  | 
**StoreAccountId** | **string** | The store the sample comes from. | 
**ProductId** | **string** |  | 
**VariantId** | **string** |  | 
**ProductTitle** | **string** |  | 
**VariantTitle** | **string** |  | 
**ShippingAddress** | [**CampaignSampleShippingAddress**](CampaignSampleShippingAddress.md) |  | 
**Note** | **string** | The creator&#39;s note. | 
**Status** | **string** | pending: waits for review. approved: a discount code was created. shipped: you recorded that you sent it. declined: final for this request. | 
**DeclineReason** | **string** |  | 
**DiscountCode** | **string** | The 100%-off, single-use code for the product, set on approval. | 
**TrackingUrl** | **string** |  | 
**ApprovedAt** | **DateTime?** |  | 
**ShippedAt** | **DateTime?** |  | 
**RequestedAt** | **DateTime** |  | 
**ContentDueAt** | **DateTime?** | When a post is due: the approval plus the campaign&#39;s &#x60;sampleContentDueDays&#x60;. Null unless approved or shipped. | 
**ContentOwed** | **bool** | True past &#x60;contentDueAt&#x60; when the creator submitted no post since the approval. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

