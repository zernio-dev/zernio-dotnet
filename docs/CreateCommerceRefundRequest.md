# Zernio.Model.CreateCommerceRefundRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | Connected store SocialAccount id. | 
**LineItems** | [**List&lt;CommerceRefundRequestLineItemsInner&gt;**](CommerceRefundRequestLineItemsInner.md) |  | [optional] 
**Shipping** | [**CommerceRefundRequestShipping**](CommerceRefundRequestShipping.md) |  | [optional] 
**Amount** | **string** | Refund this much money instead of what the lines and shipping are worth, for a goodwill refund or a partial one. Taken from the order&#39;s payments in order, up to what each can still refund. | [optional] 
**Currency** | **string** | The currency your amounts are in. Refused (400) unless it is the one the buyer paid in, which every refund amount uses. | [optional] 
**Note** | **string** | Kept on the refund, visible to staff. | [optional] 
**NotifyCustomer** | **bool** | Email the buyer about the refund. | [optional] [default to false]
**ValidateOnly** | **bool** | Return the refund the platform would make, without refunding anything. | [optional] [default to false]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

