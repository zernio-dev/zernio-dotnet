# Zernio.Model.ListCampaignOrders200ResponseOrdersInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**PlatformOrderId** | **string** | The order id on the store, as in &#x60;GET /v1/commerce/orders/{orderId}&#x60;. | 
**OrderNumber** | **string** |  | 
**Status** | **string** |  | 
**ParticipantId** | **string** |  | 
**CreatorName** | **string** |  | 
**CreatorAvatarUrl** | **string** | The creator&#39;s profile picture. Same source as a participant&#39;s &#x60;creator.avatarUrl&#x60;. | 
**MatchedBy** | **string** |  | 
**DiscountCode** | **string** |  | 
**Currency** | **string** |  | 
**SalesCents** | **int** |  | 
**RefundedCents** | **int** |  | 
**CommissionCents** | **int** | Commission the order holds now, net of refunds. | 
**OrderCreatedAt** | **DateTime** |  | 
**ApprovedAt** | **DateTime?** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

