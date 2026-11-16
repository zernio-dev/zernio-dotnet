# Zernio.Model.WebhookPayloadAccountPrivacyRequestPrivacyRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** | customer_data_request: the merchant asked for the data you hold about &#x60;customer&#x60;. Send it to the merchant.  customer_redact: erase the data you hold about &#x60;customer&#x60; and the orders in &#x60;orderIds&#x60;.  shop_redact: erase the data you hold about the whole shop. Sent 48 hours after the merchant uninstalled the app. | 
**ShopDomain** | **string** |  | 
**ShopId** | **string** |  | 
**Customer** | [**WebhookPayloadAccountPrivacyRequestPrivacyRequestCustomer**](WebhookPayloadAccountPrivacyRequestPrivacyRequestCustomer.md) |  | 
**OrderIds** | **List&lt;string&gt;** | The Shopify order ids the request covers. Empty for shop_redact. | 
**DataRequestId** | **string** | Shopify&#39;s id for a customer_data_request. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

